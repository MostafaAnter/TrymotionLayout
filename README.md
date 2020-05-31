# TrymotionLayout
# To start motionLayout programically i used this snipt 

    private fun coordinateMotion() {
        val appBarLayout: AppBarLayout = findViewById(R.id.appbar_layout)
        val motionLayout: MotionLayout = findViewById(R.id.motion_layout)

        val listener = AppBarLayout.OnOffsetChangedListener { unused, verticalOffset ->
            val seekPosition = -verticalOffset / appBarLayout.totalScrollRange.toFloat()
            motionLayout.progress = seekPosition
        }

        appBarLayout.addOnOffsetChangedListener(listener)
    }
    
##     To scal views i add KeyFrameSet to my Transition

    <KeyFrameSet>
           <KeyAttribute
               android:scaleX="0.5"
               android:scaleY="0.5"
               motion:framePosition="100"
               motion:motionTarget="@id/avatar"
               />
       </KeyFrameSet>
