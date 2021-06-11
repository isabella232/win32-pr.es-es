---
description: Obtenga información sobre cómo la propiedad System.GPS.DestLatitude indica la latitud del punto de destino.
ms.assetid: 63d8a3a3-76ec-4121-b48b-eb5034117d04
title: System.GPS.DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbed51e89926b8bb505457bd9fd7bf7bd3b69ff2
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988970"
---
# <a name="systemgpsdestlatitude"></a><span data-ttu-id="13e81-103">System.GPS.DestLatitude</span><span class="sxs-lookup"><span data-stu-id="13e81-103">System.GPS.DestLatitude</span></span>

<span data-ttu-id="13e81-104">Indica la latitud del punto de destino.</span><span class="sxs-lookup"><span data-stu-id="13e81-104">Indicates the latitude of the destination point.</span></span> <span data-ttu-id="13e81-105">Se trata de una matriz de tres valores, como se muestra a continuación: el índice 0 es el grado, el índice 1 son los minutos, el índice 2 son los segundos.</span><span class="sxs-lookup"><span data-stu-id="13e81-105">This is an array of three values, as follows: index 0 is the degrees, index 1 is the minutes, index 2 is the seconds.</span></span> <span data-ttu-id="13e81-106">Cada se calcula a partir de los valores de PKEY \_ GPS \_ DestLatitudeNumerator y PKEY \_ GPS \_ DestLatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="13e81-106">Each is calculated from the values in PKEY\_GPS\_DestLatitudeNumerator and PKEY\_GPS\_DestLatitudeDenominator.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="13e81-107">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13e81-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.GPS.DestLatitude
   shellPKey = PKEY_GPS_DestLatitude
   formatID = 9D1D7CC5-5C39-451C-86B3-928E2D18CC47
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="13e81-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13e81-108">Remarks</span></span>

<span data-ttu-id="13e81-109">Los valores PKEY se definen en Propkey.h.</span><span class="sxs-lookup"><span data-stu-id="13e81-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13e81-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13e81-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e81-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="13e81-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="13e81-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="13e81-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="13e81-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="13e81-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="13e81-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="13e81-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="13e81-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="13e81-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="13e81-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="13e81-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="13e81-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="13e81-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="13e81-118">numberFormat</span><span class="sxs-lookup"><span data-stu-id="13e81-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="13e81-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="13e81-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="13e81-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="13e81-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="13e81-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="13e81-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="13e81-122">editControl</span><span class="sxs-lookup"><span data-stu-id="13e81-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="13e81-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="13e81-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="13e81-124">queryControl</span><span class="sxs-lookup"><span data-stu-id="13e81-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
