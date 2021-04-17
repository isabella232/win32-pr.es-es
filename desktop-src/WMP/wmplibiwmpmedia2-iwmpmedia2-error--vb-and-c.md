---
title: IWMPMedia2 (propiedad de error)
description: La propiedad error obtiene una interfaz IWMPErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Propiedad error de Windows Media Player
- Propiedad error de Windows Media Player, interfaz IWMPMedia2
- Interfaz IWMPMedia2 Windows Media Player, propiedad error
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2179b4604efd03574c78261575ce02311cd18a0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670368"
---
# <a name="iwmpmedia2error-property"></a><span data-ttu-id="7fa18-106">IWMPMedia2:: error (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7fa18-106">IWMPMedia2::Error property</span></span>

<span data-ttu-id="7fa18-107">La propiedad **error** obtiene una interfaz **IWMPErrorItem** si el elemento multimedia tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="7fa18-107">The **Error** property gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span>

<span data-ttu-id="7fa18-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fa18-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa18-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fa18-109">Syntax</span></span>


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a><span data-ttu-id="7fa18-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7fa18-110">Property value</span></span>

<span data-ttu-id="7fa18-111">Una interfaz **WMPLib. IWMPErrorItem** que proporciona acceso a información sobre la condición de error.</span><span class="sxs-lookup"><span data-stu-id="7fa18-111">A **WMPLib.IWMPErrorItem** interface that provides access to information about the error condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fa18-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fa18-112">Remarks</span></span>

<span data-ttu-id="7fa18-113">Si no se puede reproducir el elemento multimedia, esta propiedad obtiene una interfaz **IWMPErrorItem** que contiene información sobre el problema encontrado.</span><span class="sxs-lookup"><span data-stu-id="7fa18-113">If the media item cannot be played, this property gets an **IWMPErrorItem** interface that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa18-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa18-114">Requirements</span></span>



| <span data-ttu-id="7fa18-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa18-115">Requirement</span></span> | <span data-ttu-id="7fa18-116">Value</span><span class="sxs-lookup"><span data-stu-id="7fa18-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa18-117">Versión</span><span class="sxs-lookup"><span data-stu-id="7fa18-117">Version</span></span><br/>   | <span data-ttu-id="7fa18-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="7fa18-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7fa18-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7fa18-119">Namespace</span></span><br/> | <span data-ttu-id="7fa18-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7fa18-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7fa18-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="7fa18-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7fa18-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7fa18-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa18-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fa18-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa18-124">**IWMPErrorItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7fa18-124">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7fa18-125">**Interfaz IWMPMedia2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7fa18-125">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





