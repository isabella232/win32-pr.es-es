---
description: 'Vuelve a crear los datos de propiedad internos y específicos de la aplicación para una matriz de bytes que se creó anteriormente con IContextNode:: SavePropertiesData.'
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'IContextNode:: LoadPropertiesData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696530"
---
# <a name="icontextnodeloadpropertiesdata-method"></a><span data-ttu-id="0a070-103">IContextNode:: LoadPropertiesData (método)</span><span class="sxs-lookup"><span data-stu-id="0a070-103">IContextNode::LoadPropertiesData method</span></span>

<span data-ttu-id="0a070-104">Vuelve a crear los datos de propiedad internos y específicos de la aplicación para una matriz de bytes que se creó anteriormente con [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="0a070-104">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a070-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a070-105">Syntax</span></span>


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="0a070-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a070-107">*cbPropertiesDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a070-107">*cbPropertiesDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a070-108">Tamaño de la matriz de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0a070-108">The size of the properties data array.</span></span>

</dd> <dt>

<span data-ttu-id="0a070-109">*pbPropertiesData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a070-109">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a070-110">Matriz de enteros de 8 bits sin signo que contiene la información de propiedad que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="0a070-110">The 8-bit unsigned integer array containing property information to load.</span></span>

</dd> <dt>

<span data-ttu-id="0a070-111">*pfSuccessful* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a070-111">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a070-112">**Variante \_ TRUE** si los datos de la propiedad se cargaron correctamente; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="0a070-112">**VARIANT\_TRUE** if the property data loaded successfully; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a070-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a070-113">Return value</span></span>

<span data-ttu-id="0a070-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0a070-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a070-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a070-115">Requirements</span></span>



| <span data-ttu-id="0a070-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a070-116">Requirement</span></span> | <span data-ttu-id="0a070-117">Value</span><span class="sxs-lookup"><span data-stu-id="0a070-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a070-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a070-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0a070-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0a070-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0a070-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a070-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0a070-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0a070-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0a070-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a070-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a070-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0a070-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0a070-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a070-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a070-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a070-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0a070-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a070-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a070-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="0a070-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0a070-128">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a070-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="0a070-129">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a070-129">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="0a070-130">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a070-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="0a070-131">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="0a070-131">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="0a070-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a070-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="0a070-133">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="0a070-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="0a070-134">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="0a070-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




