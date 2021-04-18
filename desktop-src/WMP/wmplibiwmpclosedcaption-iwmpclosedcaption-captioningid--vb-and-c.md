---
title: Propiedad captioningId de IWMPClosedCaption
description: La propiedad IWMPClosedCaption obtiene o establece el nombre del elemento HTML que muestra los subtítulos.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- propiedades de captioningId Media Player de Windows
- propiedad captioningId de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649910"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a><span data-ttu-id="27171-106">IWMPClosedCaption:: captioningId (propiedad)</span><span class="sxs-lookup"><span data-stu-id="27171-106">IWMPClosedCaption::captioningId property</span></span>

<span data-ttu-id="27171-107">La propiedad **IWMPClosedCaption** obtiene o establece el nombre del elemento HTML que muestra los subtítulos.</span><span class="sxs-lookup"><span data-stu-id="27171-107">The **IWMPClosedCaption** property gets or sets the name of the HTML element displaying the captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="27171-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27171-108">Syntax</span></span>


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a><span data-ttu-id="27171-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="27171-109">Property value</span></span>

<span data-ttu-id="27171-110">**System. String** que es el identificador del elemento HTML.</span><span class="sxs-lookup"><span data-stu-id="27171-110">The **System.String** that is the ID of the HTML element.</span></span>

## <a name="remarks"></a><span data-ttu-id="27171-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27171-111">Remarks</span></span>

<span data-ttu-id="27171-112">El nombre de elemento especificado puede ser cualquier elemento HTML de la página web siempre que admita el atributo **innerHTML** .</span><span class="sxs-lookup"><span data-stu-id="27171-112">The element name specified can be any HTML element in the webpage as long as it supports the **innerHTML** attribute.</span></span> <span data-ttu-id="27171-113">Si la página web contiene varios marcos, el nombre del elemento solo puede hacer referencia a un elemento del mismo marco que el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="27171-113">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="27171-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27171-114">Requirements</span></span>



| <span data-ttu-id="27171-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="27171-115">Requirement</span></span> | <span data-ttu-id="27171-116">Value</span><span class="sxs-lookup"><span data-stu-id="27171-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27171-117">Versión</span><span class="sxs-lookup"><span data-stu-id="27171-117">Version</span></span><br/>   | <span data-ttu-id="27171-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="27171-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="27171-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27171-119">Namespace</span></span><br/> | <span data-ttu-id="27171-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="27171-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="27171-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="27171-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="27171-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="27171-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27171-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="27171-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27171-124">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="27171-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="27171-125">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="27171-125">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="27171-126">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="27171-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





