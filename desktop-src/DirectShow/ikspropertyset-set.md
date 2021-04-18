---
description: El método Set establece una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'IKsPropertySet:: set (método) (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422890"
---
# <a name="ikspropertysetset-method"></a><span data-ttu-id="74308-103">IKsPropertySet:: set (método)</span><span class="sxs-lookup"><span data-stu-id="74308-103">IKsPropertySet::Set method</span></span>

<span data-ttu-id="74308-104">El `Set` método establece una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="74308-104">The `Set` method sets a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="74308-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74308-105">Syntax</span></span>


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a><span data-ttu-id="74308-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74308-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74308-107">*guidPropSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74308-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74308-108">GUID del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="74308-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="74308-109">*dwPropID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74308-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74308-110">Identificador de la propiedad dentro del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="74308-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="74308-111">*pInstanceData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74308-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74308-112">Puntero a un búfer que contiene datos de instancia para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="74308-112">Pointer to a buffer that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="74308-113">*cbInstanceData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74308-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74308-114">Tamaño del búfer de *pInstanceData* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="74308-114">Size of the *pInstanceData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="74308-115">*pPropData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74308-115">*pPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74308-116">Puntero a un búfer que contiene el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="74308-116">Pointer to a buffer that contains the value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="74308-117">*cbPropData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74308-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74308-118">Sise del búfer *pPropData* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="74308-118">Sise of the *pPropData* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74308-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74308-119">Return value</span></span>

<span data-ttu-id="74308-120">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="74308-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="74308-121">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="74308-121">Possible values include the following.</span></span>



| <span data-ttu-id="74308-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="74308-122">Return code</span></span>                                                                                              | <span data-ttu-id="74308-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="74308-123">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74308-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="74308-124"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="74308-125">Correcto.</span><span class="sxs-lookup"><span data-stu-id="74308-125">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="74308-126"><dt>**E \_ prop \_ set \_ no compatible**</dt></span><span class="sxs-lookup"><span data-stu-id="74308-126"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="74308-127">No se admite el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="74308-127">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="74308-128"><dt>**E \_ \_ ID. de prop \_ no compatible**</dt></span><span class="sxs-lookup"><span data-stu-id="74308-128"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="74308-129">El identificador de propiedad no es compatible con el conjunto de propiedades especificado.</span><span class="sxs-lookup"><span data-stu-id="74308-129">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74308-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74308-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74308-131">Existe otra interfaz con este nombre en el archivo de encabezado dsound. h.</span><span class="sxs-lookup"><span data-stu-id="74308-131">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="74308-132">Las dos interfaces no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="74308-132">The two interfaces are not compatible.</span></span> <span data-ttu-id="74308-133">La interfaz **IKsControl** , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="74308-133">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="74308-134">Debe incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="74308-134">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="74308-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74308-135">Requirements</span></span>



| <span data-ttu-id="74308-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="74308-136">Requirement</span></span> | <span data-ttu-id="74308-137">Value</span><span class="sxs-lookup"><span data-stu-id="74308-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74308-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74308-138">Minimum supported client</span></span><br/> | <span data-ttu-id="74308-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="74308-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74308-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74308-140">Minimum supported server</span></span><br/> | <span data-ttu-id="74308-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74308-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74308-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74308-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="74308-143"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="74308-143"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="74308-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74308-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="74308-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74308-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74308-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="74308-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74308-147">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="74308-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="74308-148">**Interfaz IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="74308-148">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="74308-149">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="74308-149">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




