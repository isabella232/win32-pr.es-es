---
title: IWMPCdromBurn Erase (método)
description: El método Erase borra el CD actual.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- borrado de ventanas de método Media Player
- borrar el método Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, método Erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718833"
---
# <a name="iwmpcdromburnerase-method"></a><span data-ttu-id="f3ee1-106">IWMPCdromBurn:: Erase (método)</span><span class="sxs-lookup"><span data-stu-id="f3ee1-106">IWMPCdromBurn::erase method</span></span>

<span data-ttu-id="f3ee1-107">El método **Erase** borra el CD actual.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-107">The **erase** method erases the current CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ee1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3ee1-108">Syntax</span></span>


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a><span data-ttu-id="f3ee1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3ee1-109">Parameters</span></span>

<span data-ttu-id="f3ee1-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3ee1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3ee1-111">Return value</span></span>

<span data-ttu-id="f3ee1-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ee1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3ee1-113">Remarks</span></span>

<span data-ttu-id="f3ee1-114">Este método no funcionará si no se reescribirá el disco de la unidad.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-114">This method will not work if the disc in the drive is not rewritable.</span></span> <span data-ttu-id="f3ee1-115">Use [IWMPCdromBurn. isavailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) para determinar si se puede borrar un CD.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-115">Use [IWMPCdromBurn.isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) to determine whether a CD can be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ee1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3ee1-116">Requirements</span></span>



| <span data-ttu-id="f3ee1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ee1-117">Requirement</span></span> | <span data-ttu-id="f3ee1-118">Value</span><span class="sxs-lookup"><span data-stu-id="f3ee1-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ee1-119">Versión</span><span class="sxs-lookup"><span data-stu-id="f3ee1-119">Version</span></span><br/>   | <span data-ttu-id="f3ee1-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f3ee1-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="f3ee1-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3ee1-121">Namespace</span></span><br/> | <span data-ttu-id="f3ee1-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f3ee1-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f3ee1-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="f3ee1-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f3ee1-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f3ee1-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ee1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3ee1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ee1-126">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f3ee1-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





