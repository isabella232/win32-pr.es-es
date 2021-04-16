---
title: Propiedad ripProgress de IWMPCdromRip
description: La propiedad ripProgress obtiene el progreso de la copia de CD como porcentaje completado.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- propiedades de ripProgress Media Player de Windows
- propiedad ripProgress de Windows Media Player, interfaz IWMPCdromRip
- Interfaz IWMPCdromRip Windows Media Player, propiedad ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718805"
---
# <a name="iwmpcdromripripprogress-property"></a><span data-ttu-id="c8b44-106">IWMPCdromRip:: ripProgress (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c8b44-106">IWMPCdromRip::ripProgress property</span></span>

<span data-ttu-id="c8b44-107">La propiedad **ripProgress** obtiene el progreso de la copia de CD como porcentaje completado.</span><span class="sxs-lookup"><span data-stu-id="c8b44-107">The **ripProgress** property gets the CD ripping progress as percent complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b44-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8b44-108">Syntax</span></span>


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="c8b44-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c8b44-109">Property value</span></span>

<span data-ttu-id="c8b44-110">**System. Int32** que es el valor de progreso.</span><span class="sxs-lookup"><span data-stu-id="c8b44-110">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="c8b44-111">Los valores de progreso oscilan entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="c8b44-111">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8b44-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8b44-112">Remarks</span></span>

<span data-ttu-id="c8b44-113">El valor de progreso representa el porcentaje completado de todo el proceso de copia.</span><span class="sxs-lookup"><span data-stu-id="c8b44-113">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="c8b44-114">Para determinar el progreso de una pista concreta, use [IWMPMedia. getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) con **RipProgress** como nombre de atributo.</span><span class="sxs-lookup"><span data-stu-id="c8b44-114">To determine the progress of a specific track, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) with **RipProgress** as the attribute name.</span></span> <span data-ttu-id="c8b44-115">Para obtener el índice de la pista que se está copiando actualmente, llame a IWMPPlaylist. getItemInfo con "CurrentRipTrackIndex" como nombre de atributo.</span><span class="sxs-lookup"><span data-stu-id="c8b44-115">To get the index of the track currently being ripped, call IWMPPlaylist.getItemInfo with "CurrentRipTrackIndex" as the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b44-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8b44-116">Requirements</span></span>



| <span data-ttu-id="c8b44-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b44-117">Requirement</span></span> | <span data-ttu-id="c8b44-118">Value</span><span class="sxs-lookup"><span data-stu-id="c8b44-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b44-119">Versión</span><span class="sxs-lookup"><span data-stu-id="c8b44-119">Version</span></span><br/>   | <span data-ttu-id="c8b44-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="c8b44-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="c8b44-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8b44-121">Namespace</span></span><br/> | <span data-ttu-id="c8b44-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c8b44-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c8b44-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c8b44-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c8b44-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c8b44-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b44-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8b44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b44-126">**Interfaz IWMPCdromRip (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c8b44-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8b44-127">**Copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="c8b44-127">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





