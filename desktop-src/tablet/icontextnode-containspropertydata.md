---
description: Determina si el objeto IContextNode contiene datos almacenados en el identificador especificado.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'IContextNode:: ContainsPropertyData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497590"
---
# <a name="icontextnodecontainspropertydata-method"></a><span data-ttu-id="a6ddb-103">IContextNode:: ContainsPropertyData (método)</span><span class="sxs-lookup"><span data-stu-id="a6ddb-103">IContextNode::ContainsPropertyData method</span></span>

<span data-ttu-id="a6ddb-104">Determina si el objeto [**IContextNode**](icontextnode.md) contiene datos almacenados en el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="a6ddb-104">Determines whether the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ddb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6ddb-105">Syntax</span></span>


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a><span data-ttu-id="a6ddb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6ddb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ddb-107">*pPropertyDataId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6ddb-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ddb-108">El identificador de los datos.</span><span class="sxs-lookup"><span data-stu-id="a6ddb-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="a6ddb-109">*pbContains* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a6ddb-109">*pbContains* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ddb-110">**Variante \_ TRUE** si el objeto [**IContextNode**](icontextnode.md) contiene datos almacenados en el identificador especificado; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a6ddb-110">**VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ddb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6ddb-111">Return value</span></span>

<span data-ttu-id="a6ddb-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a6ddb-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6ddb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6ddb-113">Remarks</span></span>

<span data-ttu-id="a6ddb-114">Además de los datos específicos de la aplicación, también puede usar este método para determinar si este [**IContextNode**](icontextnode.md) contiene otros datos internos (consulte [propiedades](analysis-hint-properties.md) de la sugerencia de análisis y [propiedades del nodo de contexto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="a6ddb-114">In addition to application-specific data, you can also use this method to determine whether this [**IContextNode**](icontextnode.md) contains other internal data (see [Analysis Hint Properties](analysis-hint-properties.md) and [Context Node Properties](context-node-properties.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ddb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6ddb-115">Requirements</span></span>



| <span data-ttu-id="a6ddb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ddb-116">Requirement</span></span> | <span data-ttu-id="a6ddb-117">Value</span><span class="sxs-lookup"><span data-stu-id="a6ddb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ddb-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6ddb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ddb-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a6ddb-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a6ddb-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6ddb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ddb-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a6ddb-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a6ddb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6ddb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ddb-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ddb-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a6ddb-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6ddb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ddb-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ddb-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a6ddb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6ddb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ddb-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a6ddb-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a6ddb-128">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a6ddb-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a6ddb-129">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a6ddb-129">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a6ddb-130">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="a6ddb-130">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="a6ddb-131">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="a6ddb-131">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="a6ddb-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="a6ddb-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="a6ddb-133">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="a6ddb-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="a6ddb-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a6ddb-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




