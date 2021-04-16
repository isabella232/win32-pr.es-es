---
title: ClosedCaption.SAMILangCount
description: La propiedad SAMILangCount recupera el número de idiomas admitidos por el archivo SAMI actual.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- ClosedCaption. SAMILangCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699536"
---
# <a name="closedcaptionsamilangcount"></a><span data-ttu-id="f36f1-104">ClosedCaption.SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="f36f1-104">ClosedCaption.SAMILangCount</span></span>

<span data-ttu-id="f36f1-105">La propiedad **SAMILangCount** recupera el número de idiomas admitidos por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="f36f1-105">The **SAMILangCount** property retrieves the number of languages supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a><span data-ttu-id="f36f1-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f36f1-106">Possible Values</span></span>

<span data-ttu-id="f36f1-107">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="f36f1-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f36f1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f36f1-108">Remarks</span></span>

<span data-ttu-id="f36f1-109">Este método no se puede usar hasta que se abra un archivo multimedia digital (*reproductor*.**openState** es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="f36f1-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="f36f1-110">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="f36f1-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f36f1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f36f1-111">Requirements</span></span>



| <span data-ttu-id="f36f1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36f1-112">Requirement</span></span> | <span data-ttu-id="f36f1-113">Value</span><span class="sxs-lookup"><span data-stu-id="f36f1-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f36f1-114">Versión</span><span class="sxs-lookup"><span data-stu-id="f36f1-114">Version</span></span><br/> | <span data-ttu-id="f36f1-115">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="f36f1-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f36f1-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f36f1-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="f36f1-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f36f1-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f36f1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f36f1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36f1-119">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="f36f1-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f36f1-120">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="f36f1-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="f36f1-121">**ClosedCaption.getSAMILangName**</span><span class="sxs-lookup"><span data-stu-id="f36f1-121">**ClosedCaption.getSAMILangName**</span></span>](closedcaption-getsamilangname.md)
</dt> <dt>

[<span data-ttu-id="f36f1-122">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="f36f1-122">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





