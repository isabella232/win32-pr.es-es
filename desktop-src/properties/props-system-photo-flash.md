---
description: Un indicador del estado de Flash en el que se tomó la foto, como se lee en la información del archivo de imagen intercambiable (EXIF).
ms.assetid: e21de610-9916-4b3f-8e50-f0141b476346
title: System. Photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af98011f8b5e5907387fe53c7495d5e6cd30fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276560"
---
# <a name="systemphotoflash"></a><span data-ttu-id="e309f-103">System. Photo. Flash</span><span class="sxs-lookup"><span data-stu-id="e309f-103">System.Photo.Flash</span></span>

<span data-ttu-id="e309f-104">Un indicador del estado de Flash en el que se tomó la foto, como se lee en la información del archivo de imagen intercambiable (EXIF).</span><span class="sxs-lookup"><span data-stu-id="e309f-104">An indicator of the flash status when the photo was taken, as read from the Exchangeable Image File (EXIF) info.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e309f-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e309f-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Flash
   shellPKey = PKEY_Photo_Flash
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37385
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Byte
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NoFlash
            value = 0
            text = No flash
            defineToken = PHOTO_FLASH_NONE
         enum
            name = Flash
            value = 1
            text = Flash
            defineToken = PHOTO_FLASH_FLASH
         enum
            name = FlashNoReturnLight
            value = 5
            text = Flash, no strobe return
            defineToken = PHOTO_FLASH_WITHOUTSTROBE
         enum
            name = FlashReturnLight
            value = 7
            text = Flash, strobe return
            defineToken = PHOTO_FLASH_WITHSTROBE
         enum
            name = FlashCompulsory
            value = 9
            text = Flash, compulsory
            defineToken = PHOTO_FLASH_FLASH_COMPULSORY
         enum
            name = FlashCompulsoryNoReturnLight
            value = 13
            text = Flash, compulsory, no strobe return
            defineToken = PHOTO_FLASH_FLASH_COMPULSORY_NORETURNLIGHT
         enum
            name = FlashCompulsoryReturnLight
            value = 15
            text = Flash, compulsory, strobe return
            defineToken = PHOTO_FLASH_FLASH_COMPULSORY_RETURNLIGHT
         enum
            name = NoFlashCompulsory
            value = 16
            text = No flash, compulsory
            defineToken = PHOTO_FLASH_NONE_COMPULSORY
         enum
            name = NoFlashAuto
            value = 24
            text = No flash, auto
            defineToken = PHOTO_FLASH_NONE_AUTO
         enum
            name = FlashAuto
            value = 25
            text = Flash, auto
            defineToken = PHOTO_FLASH_FLASH_AUTO
         enum
            name = FlashAutoNoReturnLight
            value = 29
            text = Flash, auto, no strobe return
            defineToken = PHOTO_FLASH_FLASH_AUTO_NORETURNLIGHT
         enum
            name = FlashAutoReturnLight
            value = 31
            text = Flash, auto, strobe return
            defineToken = PHOTO_FLASH_FLASH_AUTO_RETURNLIGHT
         enum
            name = NoFlashFunction
            value = 32
            text = No flash function
            defineToken = PHOTO_FLASH_NOFUNCTION
         enum
            name = FlashRedEye
            value = 65
            text = Flash, red-eye
            defineToken = PHOTO_FLASH_FLASH_REDEYE
         enum
            name = FlashRedEyeNoReturnLight
            value = 69
            text = Flash, red-eye, no strobe return
            defineToken = PHOTO_FLASH_FLASH_REDEYE_NORETURNLIGHT
         enum
            name = FlashRedEyeReturnLight
            value = 71
            text = Flash, red-eye, strobe return
            defineToken = PHOTO_FLASH_FLASH_REDEYE_RETURNLIGHT
         enum
            name = FlashCompulsoryRedEye
            value = 73
            text = Flash, compulsory, red-eye
            defineToken = PHOTO_FLASH_FLASH_COMPULSORY_REDEYE
         enum
            name = FlashCompulsoryRedEyeNoReturnLight
            value = 77
            text = Flash, compulsory, red-eye, no strobe return
            defineToken = PHOTO_FLASH_FLASH_COMPULSORY_REDEYE_NORETURNLIGHT
         enum
            name = FlashCompulsoryRedEyeReturnLight
            value = 79
            text = Flash, compulsory, red-eye, strobe return
            defineToken = PHOTO_FLASH_FLASH_COMPULSORY_REDEYE_RETURNLIGHT
         enum
            name = FlashAutoRedEye
            value = 89
            text = Flash, auto, red-eye
            defineToken = PHOTO_FLASH_FLASH_AUTO_REDEYE
         enum
            name = FlashAutoRedEyeNoReturnLight
            value = 93
            text = Flash, auto, no strobe return, red-eye
            defineToken = PHOTO_FLASH_FLASH_AUTO_REDEYE_NORETURNLIGHT
         enum
            name = FlashAutoRedEyeReturnLight
            value = 95
            text = Flash, auto, strobe return, red-eye
            defineToken = PHOTO_FLASH_FLASH_AUTO_REDEYE_RETURNLIGHT
```

## <a name="windows-vista"></a><span data-ttu-id="e309f-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e309f-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Flash
   shellPKey = PKEY_Photo_Flash
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 37385
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Byte
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = No Flash
            defineName = PHOTO_FLASH_NONE
         enum
            value = 1
            text = Flash
            defineName = PHOTO_FLASH_FLASH
         enum
            value = 5
            text = Flash without strobe return
            defineName = PHOTO_FLASH_WITHOUTSTROBE
         enum
            value = 7
            text = Flash with strobe return
            defineName = PHOTO_FLASH_WITHSTROBE
         enum
            value = 9
            text = @propsys.dll,-39680
            defineName = PHOTO_FLASH_FLASH_COMPULSORY
         enum
            value = 13
            text = @propsys.dll,-39681
            defineName = PHOTO_FLASH_FLASH_COMPULSORY_NORETURNLIGHT
         enum
            value = 15
            text = @propsys.dll,-39682
            defineName = PHOTO_FLASH_FLASH_COMPULSORY_RETURNLIGHT
         enum
            value = 16
            text = @propsys.dll,-39683
            defineName = PHOTO_FLASH_NONE_COMPULSORY
         enum
            value = 24
            text = @propsys.dll,-39684
            defineName = PHOTO_FLASH_NONE_AUTO
         enum
            value = 25
            text = @propsys.dll,-39685
            defineName = PHOTO_FLASH_FLASH_AUTO
         enum
            value = 29
            text = @propsys.dll,-39686
            defineName = PHOTO_FLASH_FLASH_AUTO_NORETURNLIGHT
         enum
            value = 31
            text = @propsys.dll,-39687
            defineName = PHOTO_FLASH_FLASH_AUTO_RETURNLIGHT
         enum
            value = 32
            text = @propsys.dll,-39688
            defineName = PHOTO_FLASH_NOFUNCTION
         enum
            value = 65
            text = @propsys.dll,-39689
            defineName = PHOTO_FLASH_FLASH_REDEYE
         enum
            value = 69
            text = @propsys.dll,-39690
            defineName = PHOTO_FLASH_FLASH_REDEYE_NORETURNLIGHT
         enum
            value = 71
            text = @propsys.dll,-39691
            defineName = PHOTO_FLASH_FLASH_REDEYE_RETURNLIGHT
         enum
            value = 73
            text = @propsys.dll,-39692
            defineName = PHOTO_FLASH_FLASH_COMPULSORY_REDEYE
         enum
            value = 77
            text = @propsys.dll,-39693
            defineName = PHOTO_FLASH_FLASH_COMPULSORY_REDEYE_NORETURNLIGHT
         enum
            value = 79
            text = @propsys.dll,-39694
            defineName = PHOTO_FLASH_FLASH_COMPULSORY_REDEYE_RETURNLIGHT
         enum
            value = 89
            text = @propsys.dll,-39695
            defineName = PHOTO_FLASH_FLASH_AUTO_REDEYE
         enum
            value = 93
            text = @propsys.dll,-39696
            defineName = PHOTO_FLASH_FLASH_AUTO_REDEYE_NORETURNLIGHT
         enum
            value = 95
            text = @propsys.dll,-39697
            defineName = PHOTO_FLASH_FLASH_AUTO_REDEYE_RETURNLIGHT
```

## <a name="remarks"></a><span data-ttu-id="e309f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e309f-107">Remarks</span></span>

<span data-ttu-id="e309f-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="e309f-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e309f-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e309f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e309f-110">Exchangeable Image File Format para las cámaras digitales fijas: versión Exif 2,2</span><span class="sxs-lookup"><span data-stu-id="e309f-110">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="e309f-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e309f-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e309f-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e309f-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e309f-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e309f-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e309f-114">Requerida</span><span class="sxs-lookup"><span data-stu-id="e309f-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e309f-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e309f-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e309f-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e309f-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e309f-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e309f-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e309f-118">Numérico</span><span class="sxs-lookup"><span data-stu-id="e309f-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e309f-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e309f-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e309f-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e309f-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e309f-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="e309f-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e309f-122">editControl</span><span class="sxs-lookup"><span data-stu-id="e309f-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e309f-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="e309f-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e309f-124">Consulta</span><span class="sxs-lookup"><span data-stu-id="e309f-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
