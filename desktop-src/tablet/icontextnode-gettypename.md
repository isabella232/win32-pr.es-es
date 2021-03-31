---
description: Recupera un nombre de tipo legible de este IContextNode.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'IContextNode:: GetTypeName (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154433"
---
# <a name="icontextnodegettypename-method"></a><span data-ttu-id="e77aa-103">IContextNode:: GetTypeName (método)</span><span class="sxs-lookup"><span data-stu-id="e77aa-103">IContextNode::GetTypeName method</span></span>

<span data-ttu-id="e77aa-104">Recupera un nombre de tipo legible de este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="e77aa-104">Retrieves a human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e77aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e77aa-105">Syntax</span></span>


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="e77aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e77aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e77aa-107">*pbstrContextNodeType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e77aa-107">*pbstrContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e77aa-108">Un nombre de tipo legible de este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="e77aa-108">A human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e77aa-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e77aa-109">Return value</span></span>

<span data-ttu-id="e77aa-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e77aa-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e77aa-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e77aa-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e77aa-112">Para evitar una pérdida de memoria, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) en \* *pbstrContextNodeType* cuando ya no necesite usar la cadena.</span><span class="sxs-lookup"><span data-stu-id="e77aa-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrContextNodeType* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="e77aa-113">Por ejemplo, este método establece *pbstrContextNodeType* en "InkWordNode" para un nodo de palabra de tinta (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [tipos de nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="e77aa-113">For example, this method sets *pbstrContextNodeType* to "InkWordNode" for an ink word node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e77aa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e77aa-114">Requirements</span></span>



| <span data-ttu-id="e77aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e77aa-115">Requirement</span></span> | <span data-ttu-id="e77aa-116">Value</span><span class="sxs-lookup"><span data-stu-id="e77aa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e77aa-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e77aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e77aa-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e77aa-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e77aa-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e77aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e77aa-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e77aa-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e77aa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e77aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e77aa-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e77aa-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e77aa-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e77aa-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e77aa-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e77aa-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e77aa-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e77aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e77aa-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e77aa-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e77aa-127">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="e77aa-127">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="e77aa-128">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="e77aa-128">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="e77aa-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="e77aa-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

