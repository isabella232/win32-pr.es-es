---
description: El método QuerySupported determina si un objeto admite un conjunto de propiedades especificado.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Método IKsPropertySet:: QuerySupported (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274709"
---
# <a name="ikspropertysetquerysupported-method"></a><span data-ttu-id="9f612-103">IKsPropertySet:: QuerySupported (método)</span><span class="sxs-lookup"><span data-stu-id="9f612-103">IKsPropertySet::QuerySupported method</span></span>

<span data-ttu-id="9f612-104">El `QuerySupported` método determina si un objeto admite un conjunto de propiedades especificado.</span><span class="sxs-lookup"><span data-stu-id="9f612-104">The `QuerySupported` method determines whether an object supports a specified property set.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f612-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f612-105">Syntax</span></span>


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a><span data-ttu-id="9f612-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f612-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f612-107">*guidPropSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f612-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f612-108">GUID del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f612-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="9f612-109">*dwPropID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f612-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f612-110">Identificador de la propiedad dentro del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f612-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="9f612-111">*pTypeSupport* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f612-111">*pTypeSupport* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f612-112">Puntero a un valor en el que se van a almacenar marcas que indican la compatibilidad proporcionada por el controlador.</span><span class="sxs-lookup"><span data-stu-id="9f612-112">Pointer to a value in which to store flags indicating the support provided by the driver.</span></span> <span data-ttu-id="9f612-113">Entre las marcas admitidas se incluyen las siguientes.</span><span class="sxs-lookup"><span data-stu-id="9f612-113">Supported flags include the following.</span></span>



| <span data-ttu-id="9f612-114">Value</span><span class="sxs-lookup"><span data-stu-id="9f612-114">Value</span></span>                    | <span data-ttu-id="9f612-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f612-115">Description</span></span>                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f612-116">\_obtención de soporte técnico de KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="9f612-116">KSPROPERTY\_SUPPORT\_GET</span></span> | <span data-ttu-id="9f612-117">Puede recuperar la propiedad llamando al método [**IKsPropertySet:: get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="9f612-117">You can retrieve the property by calling the [**IKsPropertySet::Get**](ikspropertyset-get.md) method.</span></span> |
| <span data-ttu-id="9f612-118">\_conjunto de soporte de KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="9f612-118">KSPROPERTY\_SUPPORT\_SET</span></span> | <span data-ttu-id="9f612-119">Puede cambiar la propiedad llamando a [**IKsPropertySet:: set**](ikspropertyset-set.md).</span><span class="sxs-lookup"><span data-stu-id="9f612-119">You can change the property by calling [**IKsPropertySet::Set**](ikspropertyset-set.md).</span></span>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f612-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f612-120">Return value</span></span>

<span data-ttu-id="9f612-121">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f612-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9f612-122">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="9f612-122">Possible values include the following.</span></span>



| <span data-ttu-id="9f612-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9f612-123">Return code</span></span>                                                                                              | <span data-ttu-id="9f612-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f612-124">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f612-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9f612-125"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="9f612-126">Se admiten el conjunto de propiedades especificado y la combinación de ID. de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9f612-126">The specified property set and property ID combination is supported.</span></span><br/> |
| <dl> <span data-ttu-id="9f612-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f612-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                | <span data-ttu-id="9f612-128">No se admite el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f612-128">Property set is not supported.</span></span><br/>                                       |
| <dl> <span data-ttu-id="9f612-129"><dt>**E \_ \_ ID. de prop \_ no compatible**</dt></span><span class="sxs-lookup"><span data-stu-id="9f612-129"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="9f612-130">No se admite el identificador de propiedad para el conjunto de propiedades especificado.</span><span class="sxs-lookup"><span data-stu-id="9f612-130">Property ID is not supported for the specified property set.</span></span><br/>         |
| <dl> <span data-ttu-id="9f612-131"><dt>**E \_ prop \_ set \_ no compatible**</dt></span><span class="sxs-lookup"><span data-stu-id="9f612-131"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="9f612-132">No se admite el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f612-132">Property set is not supported.</span></span><br/>                                       |



 

## <a name="remarks"></a><span data-ttu-id="9f612-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f612-133">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f612-134">Existe otra interfaz con este nombre en el archivo de encabezado dsound. h.</span><span class="sxs-lookup"><span data-stu-id="9f612-134">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="9f612-135">Las dos interfaces no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="9f612-135">The two interfaces are not compatible.</span></span> <span data-ttu-id="9f612-136">La interfaz **IKsControl** , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="9f612-136">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="9f612-137">Debe incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="9f612-137">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f612-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f612-138">Requirements</span></span>



| <span data-ttu-id="9f612-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f612-139">Requirement</span></span> | <span data-ttu-id="9f612-140">Value</span><span class="sxs-lookup"><span data-stu-id="9f612-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f612-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f612-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9f612-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9f612-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                       |
| <span data-ttu-id="9f612-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f612-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9f612-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f612-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="9f612-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f612-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f612-146"><dt>KS. h; </dt> <dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f612-146"><dt>Ks.h; </dt> <dt>Ksproxy.h</dt></span></span> </dl> |
| <span data-ttu-id="9f612-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f612-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f612-148"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f612-148"><dt>Strmiids.lib</dt></span></span> </dl>                                                          |



## <a name="see-also"></a><span data-ttu-id="9f612-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f612-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f612-150">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9f612-150">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="9f612-151">**Interfaz IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9f612-151">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="9f612-152">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="9f612-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




