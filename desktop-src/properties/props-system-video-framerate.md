---
description: Indica la velocidad de fotogramas de la secuencia de vídeo, en fotogramas por 1000 segundos.
ms.assetid: cd5a2ae0-43ef-44e4-aa70-bca33baf2a56
title: System. video. velocidad de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbdee7991186621a9d636e2072cecafc70176d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277640"
---
# <a name="systemvideoframerate"></a><span data-ttu-id="a02f1-103">System. video. velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="a02f1-103">System.Video.FrameRate</span></span>

<span data-ttu-id="a02f1-104">Indica la velocidad de fotogramas de la secuencia de vídeo, en fotogramas por 1000 segundos.</span><span class="sxs-lookup"><span data-stu-id="a02f1-104">Indicates the frame rate for the video stream, in frames per 1000 seconds.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a02f1-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a02f1-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="a02f1-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a02f1-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Video.FrameRate
   shellPKey = PKEY_Video_FrameRate
   formatID = 64440491-4C8B-11D1-8B70-080036B11A03
   propID = 6
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="a02f1-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a02f1-107">Remarks</span></span>

<span data-ttu-id="a02f1-108">Para ayudar a reducir el error de truncamiento, esta propiedad no utiliza la medida de velocidad de fotogramas estándar de fotogramas por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="a02f1-108">To help reduce truncation error, this property does not use the standard frame rate measure of frames per second (FPS).</span></span> <span data-ttu-id="a02f1-109">En su lugar, esta propiedad mide la velocidad de fotogramas como fotogramas por 1000 segundos (FPS multiplicado por 1000).</span><span class="sxs-lookup"><span data-stu-id="a02f1-109">Instead, this property measures frame rate as frames per 1000 seconds (FPS multiplied by 1000).</span></span> <span data-ttu-id="a02f1-110">Por ejemplo, [System. video. fotogramas]() expresaría una velocidad de fotogramas de 29,97 fps como valor entero de 29970.</span><span class="sxs-lookup"><span data-stu-id="a02f1-110">For example, [System.Video.FrameRate]() would express a frame rate of 29.97 FPS as an integer value of 29970.</span></span>

<span data-ttu-id="a02f1-111">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="a02f1-111">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a02f1-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a02f1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a02f1-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a02f1-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a02f1-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a02f1-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a02f1-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a02f1-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a02f1-116">Requerida</span><span class="sxs-lookup"><span data-stu-id="a02f1-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a02f1-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a02f1-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a02f1-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a02f1-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a02f1-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a02f1-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a02f1-120">Numérico</span><span class="sxs-lookup"><span data-stu-id="a02f1-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a02f1-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a02f1-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a02f1-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a02f1-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a02f1-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="a02f1-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a02f1-124">editControl</span><span class="sxs-lookup"><span data-stu-id="a02f1-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a02f1-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="a02f1-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a02f1-126">Consulta</span><span class="sxs-lookup"><span data-stu-id="a02f1-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
