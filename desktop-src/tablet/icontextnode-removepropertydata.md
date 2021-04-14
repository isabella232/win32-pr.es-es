---
description: Quita una parte de los datos específicos de la aplicación.
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: 'IContextNode:: RemovePropertyData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4c2fd5924b206ee296c066a908d2a59b02019f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542046"
---
# <a name="icontextnoderemovepropertydata-method"></a><span data-ttu-id="d8880-103">IContextNode:: RemovePropertyData (método)</span><span class="sxs-lookup"><span data-stu-id="d8880-103">IContextNode::RemovePropertyData method</span></span>

<span data-ttu-id="d8880-104">Quita una parte de los datos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8880-104">Removes a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8880-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8880-105">Syntax</span></span>


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a><span data-ttu-id="d8880-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8880-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8880-107">*pPropertyDataId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8880-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8880-108">El identificador de los datos que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="d8880-108">The identifier of the data to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8880-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8880-109">Return value</span></span>

<span data-ttu-id="d8880-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d8880-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8880-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8880-111">Remarks</span></span>

<span data-ttu-id="d8880-112">**E \_** Se devuelve INVALIDARG si el parámetro *pPropertyDataId* es una de las constantes de [las propiedades del nodo de contexto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="d8880-112">**E\_INVALIDARG** is returned if the *pPropertyDataId* parameter is one of the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8880-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8880-113">Requirements</span></span>



| <span data-ttu-id="d8880-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8880-114">Requirement</span></span> | <span data-ttu-id="d8880-115">Value</span><span class="sxs-lookup"><span data-stu-id="d8880-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8880-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8880-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d8880-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d8880-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d8880-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8880-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d8880-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d8880-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d8880-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8880-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8880-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d8880-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d8880-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8880-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8880-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8880-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d8880-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8880-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8880-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d8880-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d8880-126">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d8880-126">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="d8880-127">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d8880-127">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="d8880-128">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="d8880-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="d8880-129">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="d8880-129">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="d8880-130">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="d8880-130">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="d8880-131">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="d8880-131">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="d8880-132">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d8880-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




