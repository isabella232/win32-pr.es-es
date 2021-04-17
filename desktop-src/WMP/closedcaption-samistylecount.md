---
title: ClosedCaption.SAMIStyleCount
description: La propiedad SAMIStyleCount recupera el número de estilos admitidos por el archivo SAMI actual.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- ClosedCaption. SAMIStyleCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698654"
---
# <a name="closedcaptionsamistylecount"></a><span data-ttu-id="ad25c-104">ClosedCaption.SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="ad25c-104">ClosedCaption.SAMIStyleCount</span></span>

<span data-ttu-id="ad25c-105">La propiedad **SAMIStyleCount** recupera el número de estilos admitidos por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="ad25c-105">The **SAMIStyleCount** property retrieves the number of styles supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a><span data-ttu-id="ad25c-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="ad25c-106">Possible Values</span></span>

<span data-ttu-id="ad25c-107">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="ad25c-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad25c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad25c-108">Remarks</span></span>

<span data-ttu-id="ad25c-109">Este método no se puede usar hasta que se abra un archivo multimedia digital (*reproductor*.**openState** es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="ad25c-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="ad25c-110">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="ad25c-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad25c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad25c-111">Requirements</span></span>



| <span data-ttu-id="ad25c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad25c-112">Requirement</span></span> | <span data-ttu-id="ad25c-113">Value</span><span class="sxs-lookup"><span data-stu-id="ad25c-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad25c-114">Versión</span><span class="sxs-lookup"><span data-stu-id="ad25c-114">Version</span></span><br/> | <span data-ttu-id="ad25c-115">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="ad25c-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ad25c-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad25c-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="ad25c-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad25c-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad25c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad25c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad25c-119">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="ad25c-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="ad25c-120">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="ad25c-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="ad25c-121">**ClosedCaption.getSAMIStyleName**</span><span class="sxs-lookup"><span data-stu-id="ad25c-121">**ClosedCaption.getSAMIStyleName**</span></span>](closedcaption-getsamistylename.md)
</dt> <dt>

[<span data-ttu-id="ad25c-122">**ClosedCaption.SAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="ad25c-122">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





