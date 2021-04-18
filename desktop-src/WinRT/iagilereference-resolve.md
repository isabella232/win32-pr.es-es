---
description: Obtiene el identificador de interfaz de una referencia ágil a un objeto.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'IAgileReference:: Resolve (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705669"
---
# <a name="iagilereferenceresolve-method"></a><span data-ttu-id="f785b-103">IAgileReference:: Resolve (método)</span><span class="sxs-lookup"><span data-stu-id="f785b-103">IAgileReference::Resolve method</span></span>

<span data-ttu-id="f785b-104">Obtiene el identificador de interfaz de una referencia ágil a un objeto.</span><span class="sxs-lookup"><span data-stu-id="f785b-104">Gets the interface ID of an agile reference to an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f785b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f785b-105">Syntax</span></span>


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a><span data-ttu-id="f785b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f785b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f785b-107">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f785b-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f785b-108">IDENTIFICADOR de interfaz de la interfaz que se va a recuperar de la referencia ágil.</span><span class="sxs-lookup"><span data-stu-id="f785b-108">The interface ID of the interface to be retrieved from the agile reference.</span></span> <span data-ttu-id="f785b-109">No es necesario que sea el mismo que el de la interfaz registrada.</span><span class="sxs-lookup"><span data-stu-id="f785b-109">It is not required to be the same as the registered interface.</span></span>

</dd> <dt>

<span data-ttu-id="f785b-110">*ppvObjectReference* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f785b-110">*ppvObjectReference* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f785b-111">Si se completa correctamente, \* *ppvObjectReference* es un puntero a la interfaz especificada por *riid*.</span><span class="sxs-lookup"><span data-stu-id="f785b-111">On successful completion, \**ppvObjectReference* is a pointer to the interface specified by *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f785b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f785b-112">Return value</span></span>

<span data-ttu-id="f785b-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f785b-113">This method can return one of these values.</span></span>



| <span data-ttu-id="f785b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f785b-114">Return value</span></span>                                                                              | <span data-ttu-id="f785b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f785b-115">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f785b-116"><dt>S \_ correcto</dt></span><span class="sxs-lookup"><span data-stu-id="f785b-116"><dt>S\_OK</dt></span></span> </dl>          | <span data-ttu-id="f785b-117">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f785b-117">The method completed successfully.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f785b-118"><dt>E \_ NOinterface</dt></span><span class="sxs-lookup"><span data-stu-id="f785b-118"><dt>E\_NOINTERFACE</dt></span></span> </dl> | <span data-ttu-id="f785b-119">La interfaz solicitada no está implementada en el objeto registrado.</span><span class="sxs-lookup"><span data-stu-id="f785b-119">The requested interface isn't implemented on the registered object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f785b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f785b-120">Remarks</span></span>

<span data-ttu-id="f785b-121">Llame a la función [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) para crear una referencia ágil a un objeto.</span><span class="sxs-lookup"><span data-stu-id="f785b-121">Call the [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) function to create an agile reference to an object.</span></span> <span data-ttu-id="f785b-122">Llame al método **Resolve** para localizar el objeto en el contenedor en el que se llama a **Resolve** .</span><span class="sxs-lookup"><span data-stu-id="f785b-122">Call the **Resolve** method to localize the object into the apartment in which **Resolve** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f785b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f785b-123">Requirements</span></span>



| <span data-ttu-id="f785b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f785b-124">Requirement</span></span> | <span data-ttu-id="f785b-125">Value</span><span class="sxs-lookup"><span data-stu-id="f785b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f785b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f785b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f785b-127">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f785b-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>            |
| <span data-ttu-id="f785b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f785b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f785b-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f785b-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f785b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f785b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f785b-131">**IAgileReference**</span><span class="sxs-lookup"><span data-stu-id="f785b-131">**IAgileReference**</span></span>](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[<span data-ttu-id="f785b-132">**RoGetAgileReference**</span><span class="sxs-lookup"><span data-stu-id="f785b-132">**RoGetAgileReference**</span></span>](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




