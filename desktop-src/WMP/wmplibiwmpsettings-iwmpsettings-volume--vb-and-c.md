---
title: Propiedad de volumen IWMPSettings
description: La propiedad de volumen obtiene o establece el volumen de reproducción actual.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Media Player de propiedades de volumen de Windows
- propiedad de volumen Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad de volumen
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690154"
---
# <a name="iwmpsettingsvolume-property"></a><span data-ttu-id="ad87d-106">IWMPSettings:: Volume (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ad87d-106">IWMPSettings::volume property</span></span>

<span data-ttu-id="ad87d-107">La propiedad de **volumen** obtiene o establece el volumen de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="ad87d-107">The **volume** property gets or sets the current playback volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad87d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad87d-108">Syntax</span></span>


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ad87d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ad87d-109">Property value</span></span>

<span data-ttu-id="ad87d-110">**System. Int32** que es el nivel de volumen, comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="ad87d-110">A **System.Int32** that is the volume level, ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad87d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad87d-111">Remarks</span></span>

<span data-ttu-id="ad87d-112">Un valor de cero no especifica ningún volumen (silenciado).</span><span class="sxs-lookup"><span data-stu-id="ad87d-112">A value of zero specifies no volume (muted).</span></span> <span data-ttu-id="ad87d-113">Un valor de 100 especifica el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="ad87d-113">A value of 100 specifies full volume.</span></span> <span data-ttu-id="ad87d-114">Si no se especifica ningún valor para esta propiedad, toma como valor predeterminado la última configuración de volumen establecida para Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ad87d-114">If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad87d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad87d-115">Requirements</span></span>



| <span data-ttu-id="ad87d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad87d-116">Requirement</span></span> | <span data-ttu-id="ad87d-117">Value</span><span class="sxs-lookup"><span data-stu-id="ad87d-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad87d-118">Versión</span><span class="sxs-lookup"><span data-stu-id="ad87d-118">Version</span></span><br/>   | <span data-ttu-id="ad87d-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ad87d-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ad87d-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad87d-120">Namespace</span></span><br/> | <span data-ttu-id="ad87d-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ad87d-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ad87d-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ad87d-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ad87d-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ad87d-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad87d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad87d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad87d-125">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ad87d-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





