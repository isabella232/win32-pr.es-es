---
description: 'Comprueba si una extensión especificada está disponible en el equipo y puede ser utilizada por el método IWiaItem2:: GetExtension.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2:: CheckExtension (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715343"
---
# <a name="iwiaitem2checkextension-method"></a><span data-ttu-id="8b118-103">IWiaItem2:: CheckExtension (método)</span><span class="sxs-lookup"><span data-stu-id="8b118-103">IWiaItem2::CheckExtension method</span></span>

<span data-ttu-id="8b118-104">Comprueba si una extensión especificada está disponible en el equipo y puede ser utilizada por el método [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="8b118-104">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b118-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b118-105">Syntax</span></span>


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a><span data-ttu-id="8b118-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b118-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b118-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b118-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b118-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8b118-108">Type: **LONG**</span></span>

<span data-ttu-id="8b118-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b118-109">Currently unused.</span></span> <span data-ttu-id="8b118-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="8b118-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8b118-111">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b118-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b118-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8b118-112">Type: **BSTR**</span></span>

<span data-ttu-id="8b118-113">Especifica el nombre de la extensión.</span><span class="sxs-lookup"><span data-stu-id="8b118-113">Specifies the name of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="8b118-114">*riidExtensionInterface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b118-114">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b118-115">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="8b118-115">Type: **REFIID**</span></span>

<span data-ttu-id="8b118-116">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b118-116">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="8b118-117">*pbExtensionExists* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8b118-117">*pbExtensionExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b118-118">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="8b118-118">Type: \**BOOL\** _</span></span>

<span data-ttu-id="8b118-119">Recibe un puntero a un _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="8b118-119">Receives a pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8b118-120"><span id="FALSE"></span><span id="false"></span>**ES**</span><span class="sxs-lookup"><span data-stu-id="8b118-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="8b118-121">La extensión especificada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b118-121">The specified extension is not available.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8b118-122"><span id="TRUE"></span><span id="true"></span>**REALES**</span><span class="sxs-lookup"><span data-stu-id="8b118-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="8b118-123">La extensión especificada está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b118-123">The specified extension is available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b118-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b118-124">Return value</span></span>

<span data-ttu-id="8b118-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b118-125">Type: **HRESULT**</span></span>

<span data-ttu-id="8b118-126">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8b118-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b118-127">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b118-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b118-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b118-128">Remarks</span></span>

<span data-ttu-id="8b118-129">Con este método, las aplicaciones pueden comprobar si una extensión está disponible antes de llamar al método [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="8b118-129">Using this method, applications can check whether an extension is available before calling the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <span data-ttu-id="8b118-130">Además, la aplicación puede comprobar qué extensiones están disponibles sin crear conjuntamente cada una de ellas y, a continuación, decidir cuál usar.</span><span class="sxs-lookup"><span data-stu-id="8b118-130">Also, the application can check which extensions are available without co-creating each of them, and then decide which one to use.</span></span>

## <a name="examples"></a><span data-ttu-id="8b118-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8b118-131">Examples</span></span>

<span data-ttu-id="8b118-132">CheckImgFilter comprueba si el controlador tiene un filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="8b118-132">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="8b118-133">Antes de llamar al componente de vista previa, una aplicación debe asegurarse de que el controlador tiene un filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="8b118-133">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a><span data-ttu-id="8b118-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b118-134">Requirements</span></span>



| <span data-ttu-id="8b118-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b118-135">Requirement</span></span> | <span data-ttu-id="8b118-136">Value</span><span class="sxs-lookup"><span data-stu-id="8b118-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b118-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b118-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8b118-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8b118-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b118-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b118-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8b118-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b118-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8b118-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b118-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b118-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b118-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b118-143">IDL</span><span class="sxs-lookup"><span data-stu-id="8b118-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b118-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b118-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 




