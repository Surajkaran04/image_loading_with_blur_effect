# image_loading_with_blur_effect
High quality image loading with blur effect using glide



                val requestOptions = RequestOptions()
                    .diskCacheStrategy(DiskCacheStrategy.AUTOMATIC)
                    //.placeholder(thumbnailPaths[randomPos]) // Placeholder image resource
                   // .placeholder(R.drawable.ic_screen_saver_bg)
                    .error(R.drawable.ic_screen_saver_bg)

                Glide.with(this@StandByActivity)
                    .load(ApiConstant.BASE_URL_SCREEN_SAVER_IMAGE+imagePaths[position])
                    .apply(requestOptions)
                    .thumbnail(0.25f) // Thumbnail to be displayed while loading (25% of the original size)
                .placeholder(R.drawable.ic_screen_saver_bg)
                    //.placeholder(thumbnailPaths[randomPos]) // Placeholder image resource
                    .into(binding.ivScreen)




Here we can modify the thumbnail value according to requiremnet , we can set the value .5f to 1f. here 1f by default value. means that if the image file loading done then display here.
if we use .25f value then image will display when 25% image complete with blury effect

Thanks...
