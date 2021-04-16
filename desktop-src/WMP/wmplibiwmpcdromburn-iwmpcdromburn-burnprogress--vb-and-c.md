---
title: Propiedad burnProgress de IWMPCdromBurn
description: La propiedad burnProgress obtiene el progreso de la grabación del CD como porcentaje completado.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- propiedades de burnProgress Media Player de Windows
- propiedad burnProgress de Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, propiedad burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718841"
---
# <a name="iwmpcdromburnburnprogress-property"></a><span data-ttu-id="db79c-106">IWMPCdromBurn:: burnProgress (propiedad)</span><span class="sxs-lookup"><span data-stu-id="db79c-106">IWMPCdromBurn::burnProgress property</span></span>

<span data-ttu-id="db79c-107">La propiedad **burnProgress** obtiene el progreso de la grabación del CD como porcentaje completado.</span><span class="sxs-lookup"><span data-stu-id="db79c-107">The **burnProgress** property gets the CD burning progress as percent complete.</span></span>

<span data-ttu-id="db79c-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="db79c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db79c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db79c-109">Syntax</span></span>


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="db79c-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="db79c-110">Property value</span></span>

<span data-ttu-id="db79c-111">**System. Int32** que es el valor de progreso.</span><span class="sxs-lookup"><span data-stu-id="db79c-111">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="db79c-112">Los valores de progreso oscilan entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="db79c-112">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="db79c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db79c-113">Remarks</span></span>

<span data-ttu-id="db79c-114">El valor de progreso representa el porcentaje completado del proceso de grabación completo, incluidas las operaciones de almacenamiento provisional.</span><span class="sxs-lookup"><span data-stu-id="db79c-114">The progress value represents the completed percentage of the entire burning process, including any staging operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="db79c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db79c-115">Requirements</span></span>



| <span data-ttu-id="db79c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="db79c-116">Requirement</span></span> | <span data-ttu-id="db79c-117">Value</span><span class="sxs-lookup"><span data-stu-id="db79c-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db79c-118">Versión</span><span class="sxs-lookup"><span data-stu-id="db79c-118">Version</span></span><br/>   | <span data-ttu-id="db79c-119">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="db79c-119">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="db79c-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="db79c-120">Namespace</span></span><br/> | <span data-ttu-id="db79c-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="db79c-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="db79c-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="db79c-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="db79c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="db79c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db79c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="db79c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db79c-125">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="db79c-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





