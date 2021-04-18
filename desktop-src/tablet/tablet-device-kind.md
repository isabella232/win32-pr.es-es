---
description: Indica el tipo de dispositivo de Tablet PC, como un lápiz, mouse o digitalizador táctil.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Enumeración TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678486"
---
# <a name="tablet_device_kind-enumeration"></a><span data-ttu-id="e27df-103">\_Enumeración de tipo de dispositivo de tableta \_</span><span class="sxs-lookup"><span data-stu-id="e27df-103">TABLET\_DEVICE\_KIND enumeration</span></span>

<span data-ttu-id="e27df-104">Indica el tipo de dispositivo de Tablet PC, como un lápiz, mouse o digitalizador táctil.</span><span class="sxs-lookup"><span data-stu-id="e27df-104">Indicates the type of tablet device such as a pen, mouse or touch sensitive digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e27df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e27df-105">Syntax</span></span>


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a><span data-ttu-id="e27df-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e27df-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e27df-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_mouse del dispositivo de tableta gráfica \_**</span><span class="sxs-lookup"><span data-stu-id="e27df-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET\_DEVICE\_MOUSE**</span></span>
</dt> <dd>

<span data-ttu-id="e27df-108">La tableta es un mouse.</span><span class="sxs-lookup"><span data-stu-id="e27df-108">The tablet is a mouse.</span></span> <span data-ttu-id="e27df-109">Esto incluye los paneles táctiles que se encuentran en muchos equipos portátiles.</span><span class="sxs-lookup"><span data-stu-id="e27df-109">This includes touchpads found on many laptop computers.</span></span>

</dd> <dt>

<span data-ttu-id="e27df-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_lápiz del dispositivo TABLET PC \_**</span><span class="sxs-lookup"><span data-stu-id="e27df-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET\_DEVICE\_PEN**</span></span>
</dt> <dd>

<span data-ttu-id="e27df-111">La tableta emplea un lápiz y un digitalizador electromagnéticos.</span><span class="sxs-lookup"><span data-stu-id="e27df-111">The tablet utilizes an electromagnetic pen and digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="e27df-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_Touch del dispositivo de tableta \_**</span><span class="sxs-lookup"><span data-stu-id="e27df-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET\_DEVICE\_TOUCH**</span></span>
</dt> <dd>

<span data-ttu-id="e27df-113">La tableta emplea un digitalizador con distinción de toque.</span><span class="sxs-lookup"><span data-stu-id="e27df-113">The tablet utilizes a touch sensitive digitizer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e27df-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e27df-114">Requirements</span></span>



| <span data-ttu-id="e27df-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e27df-115">Requirement</span></span> | <span data-ttu-id="e27df-116">Value</span><span class="sxs-lookup"><span data-stu-id="e27df-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e27df-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e27df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e27df-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e27df-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e27df-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e27df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e27df-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e27df-120">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="e27df-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e27df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27df-122">**ITablet2:: GetDeviceKind (método)**</span><span class="sxs-lookup"><span data-stu-id="e27df-122">**ITablet2::GetDeviceKind Method**</span></span>](itablet2-getdevicekind.md)
</dt> </dl>

 

 




