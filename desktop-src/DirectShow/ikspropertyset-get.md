---
description: El método get recupera una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'IKsPropertySet:: get (método) (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495076"
---
# <a name="ikspropertysetget-method"></a><span data-ttu-id="c6fc3-103">IKsPropertySet:: get (método)</span><span class="sxs-lookup"><span data-stu-id="c6fc3-103">IKsPropertySet::Get method</span></span>

<span data-ttu-id="c6fc3-104">El método **Get** recupera una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-104">The **Get** method retrieves a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6fc3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6fc3-105">Syntax</span></span>


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a><span data-ttu-id="c6fc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6fc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6fc3-107">*guidPropSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6fc3-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fc3-108">GUID del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-108">The GUID of the property set .</span></span>

</dd> <dt>

<span data-ttu-id="c6fc3-109">*dwPropID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6fc3-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fc3-110">Identificador de la propiedad dentro del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-110">The identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="c6fc3-111">*pInstanceData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6fc3-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fc3-112">Puntero a una matriz de bytes que contiene datos de instancia para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-112">A pointer to an array of bytes that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="c6fc3-113">*cbInstanceData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6fc3-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fc3-114">Tamaño de la matriz proporcionado en *pInstanceData*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-114">The size of the array given in *pInstanceData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c6fc3-115">*pPropData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c6fc3-115">*pPropData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fc3-116">Puntero a una matriz de bytes que recibe los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-116">A pointer to an array of bytes that receives the property data.</span></span>

</dd> <dt>

<span data-ttu-id="c6fc3-117">*cbPropData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6fc3-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fc3-118">Tamaño de la matriz proporcionado en *pPropData*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-118">The size of the array given in *pPropData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c6fc3-119">*pcbReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c6fc3-119">*pcbReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fc3-120">Recibe el número de bytes que el método copia en la matriz *pPropData* .</span><span class="sxs-lookup"><span data-stu-id="c6fc3-120">Receives the number of bytes the method copies to the *pPropData* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6fc3-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6fc3-121">Return value</span></span>

<span data-ttu-id="c6fc3-122">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6fc3-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c6fc3-123">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-123">Possible values include the following.</span></span>



| <span data-ttu-id="c6fc3-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c6fc3-124">Return code</span></span>                                                                                              | <span data-ttu-id="c6fc3-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6fc3-125">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6fc3-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fc3-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="c6fc3-127">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-127">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="c6fc3-128"><dt>**E \_ prop \_ set \_ no compatible**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fc3-128"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="c6fc3-129">No se admite el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-129">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="c6fc3-130"><dt>**E \_ \_ ID. de prop \_ no compatible**</dt></span><span class="sxs-lookup"><span data-stu-id="c6fc3-130"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="c6fc3-131">El identificador de propiedad no es compatible con el conjunto de propiedades especificado.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-131">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6fc3-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6fc3-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6fc3-133">Existe otra interfaz con este nombre en el archivo de encabezado dsound. h.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-133">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="c6fc3-134">Las dos interfaces no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-134">The two interfaces are not compatible.</span></span> <span data-ttu-id="c6fc3-135">La interfaz [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-135">The [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="c6fc3-136">Para recuperar una propiedad, asigne un búfer que este método rellenará.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-136">To retrieve a property, allocate a buffer which this method will then fill in.</span></span> <span data-ttu-id="c6fc3-137">Para determinar el tamaño de búfer necesario, especifique **null** para *pPropData* y cero (0) para *cbPropData*.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-137">To determine the necessary buffer size, specify **NULL** for *pPropData* and zero (0) for *cbPropData*.</span></span> <span data-ttu-id="c6fc3-138">Este método devuelve el tamaño de búfer necesario en *pcbReturned*.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-138">This method returns the necessary buffer size in *pcbReturned*.</span></span>

<span data-ttu-id="c6fc3-139">Debe incluir KS. h antes de ksproxy. h.</span><span class="sxs-lookup"><span data-stu-id="c6fc3-139">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="c6fc3-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c6fc3-140">Examples</span></span>

<span data-ttu-id="c6fc3-141">En el ejemplo siguiente se consulta un PIN para su categoría de PIN mediante la recuperación de la propiedad de **\_ \_ categoría AMPROPERTY PIN** .</span><span class="sxs-lookup"><span data-stu-id="c6fc3-141">The following example queries a pin for its pin category, by retrieving the **AMPROPERTY\_PIN\_CATEGORY** property.</span></span> <span data-ttu-id="c6fc3-142">(Consulte [conjunto de propiedades del PIN](pin-property-set.md)).</span><span class="sxs-lookup"><span data-stu-id="c6fc3-142">(See [Pin Property Set](pin-property-set.md).)</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c6fc3-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6fc3-143">Requirements</span></span>



| <span data-ttu-id="c6fc3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6fc3-144">Requirement</span></span> | <span data-ttu-id="c6fc3-145">Value</span><span class="sxs-lookup"><span data-stu-id="c6fc3-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6fc3-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6fc3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c6fc3-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c6fc3-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6fc3-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6fc3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c6fc3-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6fc3-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6fc3-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6fc3-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6fc3-151"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6fc3-151"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="c6fc3-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6fc3-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6fc3-153"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6fc3-153"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6fc3-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6fc3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fc3-155">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="c6fc3-155">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="c6fc3-156">**Interfaz IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="c6fc3-156">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="c6fc3-157">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="c6fc3-157">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
