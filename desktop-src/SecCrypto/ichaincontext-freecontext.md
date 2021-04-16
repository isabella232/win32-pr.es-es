---
description: Libera un \_ contexto de cadena PCCERT \_ adquirido a través de la propiedad ChainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'IChainContext:: FreeContext (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690521"
---
# <a name="ichaincontextfreecontext-method"></a><span data-ttu-id="9d958-103">IChainContext:: FreeContext (método)</span><span class="sxs-lookup"><span data-stu-id="9d958-103">IChainContext::FreeContext method</span></span>

<span data-ttu-id="9d958-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="9d958-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="9d958-105">El método **FreeContext** libera un \_ contexto de cadena PCCERT \_ adquirido a través de la propiedad [**ChainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="9d958-105">The **FreeContext** method releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d958-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d958-106">Syntax</span></span>


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a><span data-ttu-id="9d958-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d958-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d958-108">*pChainContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d958-108">*pChainContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d958-109">Contexto de la \_ cadena \_ de PCCERT que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="9d958-109">The PCCERT\_CHAIN\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d958-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d958-110">Return value</span></span>

<span data-ttu-id="9d958-111">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9d958-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="9d958-112">Un valor de S \_ OK indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d958-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="9d958-113">Cualquier otro valor indica que se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="9d958-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d958-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d958-114">Remarks</span></span>

<span data-ttu-id="9d958-115">Este método no libera el contexto de la \_ cadena PCCERT \_ contenido dentro de un objeto de [**cadena**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="9d958-115">This method does not release the PCCERT\_CHAIN\_CONTEXT contained within a [**Chain**](chain.md) object.</span></span> <span data-ttu-id="9d958-116">Solo se debe usar para liberar un contexto de \_ cadena de PCCERT \_ adquirido a través de la propiedad [**ChainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="9d958-116">It should be used only to release a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d958-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d958-117">Requirements</span></span>



| <span data-ttu-id="9d958-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d958-118">Requirement</span></span> | <span data-ttu-id="9d958-119">Value</span><span class="sxs-lookup"><span data-stu-id="9d958-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d958-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9d958-120">Redistributable</span></span><br/> | <span data-ttu-id="9d958-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d958-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9d958-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d958-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="9d958-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d958-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d958-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d958-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d958-125">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="9d958-125">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




