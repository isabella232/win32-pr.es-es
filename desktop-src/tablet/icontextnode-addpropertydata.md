---
description: Agrega una parte de los datos específicos de la aplicación.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'IContextNode:: AddPropertyData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154441"
---
# <a name="icontextnodeaddpropertydata-method"></a><span data-ttu-id="71e0b-103">IContextNode:: AddPropertyData (método)</span><span class="sxs-lookup"><span data-stu-id="71e0b-103">IContextNode::AddPropertyData method</span></span>

<span data-ttu-id="71e0b-104">Agrega una parte de los datos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="71e0b-104">Adds a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71e0b-105">Syntax</span></span>


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="71e0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71e0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e0b-107">*pPropertyDataId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71e0b-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e0b-108">Identificador único global (GUID) que se usa para identificar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="71e0b-108">A globally unique identifier (GUID) that is used to identify the type of data.</span></span>

</dd> <dt>

<span data-ttu-id="71e0b-109">*ulPropertyDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71e0b-109">*ulPropertyDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e0b-110">Tamaño de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="71e0b-110">The size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="71e0b-111">*pbPropertiesData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71e0b-111">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e0b-112">\[en, el tamaño \_ es (ulPropertyDataSize)\]</span><span class="sxs-lookup"><span data-stu-id="71e0b-112">\[in, size\_is(ulPropertyDataSize)\]</span></span>

<span data-ttu-id="71e0b-113">Matriz de enteros de 8 bits sin signo que contiene la información de propiedad que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="71e0b-113">An 8-bit unsigned integer array containing the property information to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e0b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71e0b-114">Return value</span></span>

<span data-ttu-id="71e0b-115">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="71e0b-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71e0b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71e0b-116">Remarks</span></span>

<span data-ttu-id="71e0b-117">Use **IContextNode:: AddPropertyData** para asociar datos a un nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="71e0b-117">Use **IContextNode::AddPropertyData** to associate data with a context node.</span></span> <span data-ttu-id="71e0b-118">Para recuperar los datos más adelante, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="71e0b-118">To retrieve the data later, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

<span data-ttu-id="71e0b-119">El analizador de tinta puede eliminar el nodo como parte del análisis de tinta, a menos que se confirme el nodo de contexto (vea [**IContextNode:: CONFIRM**](icontextnode-confirm.md)).</span><span class="sxs-lookup"><span data-stu-id="71e0b-119">The ink analyzer may delete the node as part of ink analysis, unless the context node is confirmed (see [**IContextNode::Confirm**](icontextnode-confirm.md)).</span></span> <span data-ttu-id="71e0b-120">Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="71e0b-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71e0b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71e0b-121">Requirements</span></span>



| <span data-ttu-id="71e0b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e0b-122">Requirement</span></span> | <span data-ttu-id="71e0b-123">Value</span><span class="sxs-lookup"><span data-stu-id="71e0b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e0b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71e0b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="71e0b-125">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="71e0b-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="71e0b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71e0b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="71e0b-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="71e0b-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="71e0b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71e0b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="71e0b-129"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="71e0b-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="71e0b-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71e0b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71e0b-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71e0b-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="71e0b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="71e0b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e0b-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="71e0b-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="71e0b-134">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="71e0b-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="71e0b-135">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="71e0b-135">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="71e0b-136">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="71e0b-136">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="71e0b-137">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="71e0b-137">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="71e0b-138">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="71e0b-138">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="71e0b-139">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="71e0b-139">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




