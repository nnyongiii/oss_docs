Functions
==========

Filter Functions
-----------------------

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

.. raw:: html

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_filter
    </code>

.. py:function:: apply_filter(filter_name, intensity = 1)

    Apply a user-defined filter to an image.

   :param filter_name: The name of the filter to apply. 
   :type filter_name: str
   :param intensity: The intensity level for the filter.
   :type intensity: int
   :return: The image after applying the filter.
   :rtype: object or boolean
   
.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

.. raw:: html

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_blur
    </code>

.. py:function:: apply_blur(intensity = 1)

    Apply a blur filter to the image with a specified intensity.

   :param: intensity (optional) : The intensity of the blur filter. Default is 1. 
   :return: The image after applying the blur filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->
   
.. raw:: html

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_sharpen
    </code>

.. py:function:: apply_sharpen(intensity = 1)

    Apply a sharpen filter to the image with a specified intensity.

   :param: intensity (optional) : The intensity of the sharpen filter. Default is 1. 
   :return: The image after applying the sharpen filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

.. raw:: html

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_brighten
    </code>

.. py:function:: apply_brighten(intensity = 1)

    Apply a brighten filter to the image with a specified intensity.

   :param: intensity (optional) : The intensity of the brighten filter. Default is 1. 
   :return: The image after applying the brighten filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_darken
    </code>

.. py:function:: apply_darken()

    Apply a darken filter to the image with a specified intensity.

   :param: intensity (optional) : The intensity of the darken filter. Default is 1. 
   :return: The image after applying the darken filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_blue_tint
    </code>

.. py:function:: apply_blue_tint()

    Convert the image to grayscale and then apply a blue tint filter.

   :return: The image after applying the blue tint filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_red_tint
    </code>

.. py:function:: apply_red_tint()

    Convert the image to grayscale and then apply a red tint filter.

   :return: The image after applying the red tint filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_yellow_tint
    </code>

.. py:function:: apply_yellow_tint()

    Convert the image to grayscale and then apply a yellow tint filter.

   :return: The image after applying the yellow tint filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_pink_tint
    </code>

.. py:function:: apply_pink_tint()

    Convert the image to grayscale and then apply a pink tint filter.

   :return: The image after applying the pink tint filter.
   :rtype: image

.. raw:: html

    <br><br> <!-- 두 줄 공백 -->

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        apply_purple_tint
    </code>

.. py:function:: apply_purple_tint()

    Convert the image to grayscale and then apply a purple tint filter.

   :return: The image after applying the purplr tint filter.
   :rtype: image

.. raw:: html

    <hr> <!-- 가로 구분선 -->

``Save image Function``
------------------------

.. raw:: html

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        save_image
    </code>

.. py:function:: save_image(save_path, image_to_save=None)

    Save the image to the specified file path.
    
   :param save_path: The file path where the image will be saved.
   :return: None
   :rtype: image
   :raise ValueError: If 'save_path' is not specified or invalid.
   :example:

.. code-block:: python
        
     library.save_image(save_path, image_to_save=filtered_image)
     #Output : Image saved to 'save_path'

.. raw:: html

    <hr> <!-- 가로 구분선 -->

``Analyze and Apply Filter Function``
--------------------------------------

.. raw:: html

    <code style="font-size: 1.3em; color: blue; font-weight: bold; font-family: 'Courier New', monospace;">
        analyze_and_apply_filter
    </code>

.. py:function:: analyze_and_apply_filter()

    Analyze emotions using the FER library and apply an appropriate filter.

   :return: The filtered image or 'False'
   :rtype: image or boolean
   :raise Exception: An error occurs if no faces are detected or emotion analysis fails.
   :example:

   .. code-block:: python

      filtered_image = library.analyze_and_apply_filter()
      filtered_image.show()