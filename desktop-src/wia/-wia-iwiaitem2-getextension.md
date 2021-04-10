---
description: Obtiene las interfaces de extensión que pueden presentarse con un controlador de dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2:: GetExtension (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082149"
---
# <a name="iwiaitem2getextension-method"></a><span data-ttu-id="d5269-103">IWiaItem2:: GetExtension (método)</span><span class="sxs-lookup"><span data-stu-id="d5269-103">IWiaItem2::GetExtension method</span></span>

<span data-ttu-id="d5269-104">Obtiene las interfaces de extensión que pueden presentarse con un controlador de dispositivo de adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="d5269-104">Gets the extension interfaces that might come with a Windows Image Acquisition (WIA) 2.0 device driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5269-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5269-105">Syntax</span></span>


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a><span data-ttu-id="d5269-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5269-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5269-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5269-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5269-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="d5269-108">Type: **LONG**</span></span>

<span data-ttu-id="d5269-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="d5269-109">Currently unused.</span></span> <span data-ttu-id="d5269-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="d5269-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d5269-111">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5269-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5269-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d5269-112">Type: **BSTR**</span></span>

<span data-ttu-id="d5269-113">Especifica el nombre de la extensión a la que la aplicación que realiza la llamada requiere un puntero.</span><span class="sxs-lookup"><span data-stu-id="d5269-113">Specifies the name of the extension that the calling application requires a pointer to.</span></span>

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span data-ttu-id="d5269-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span><span class="sxs-lookup"><span data-stu-id="d5269-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span></span>


</dt> <dd>

<span data-ttu-id="d5269-115">La extensión del filtro de segmentación.</span><span class="sxs-lookup"><span data-stu-id="d5269-115">The segmentation filter extension.</span></span> <span data-ttu-id="d5269-116">Este es actualmente el único valor válido para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="d5269-116">This is currently the only valid value for this parameter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d5269-117">*riidExtensionInterface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5269-117">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5269-118">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="d5269-118">Type: **REFIID**</span></span>

<span data-ttu-id="d5269-119">Especifica el identificador de la interfaz de extensión.</span><span class="sxs-lookup"><span data-stu-id="d5269-119">Specifies the identifier of the extension interface.</span></span>

</dd> <dt>

<span data-ttu-id="d5269-120">*ppOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d5269-120">*ppOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5269-121">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="d5269-121">Type: **VOID\*\***</span></span>

<span data-ttu-id="d5269-122">Recibe la dirección de un puntero a la interfaz de extensión.</span><span class="sxs-lookup"><span data-stu-id="d5269-122">Receives the address of a pointer to the extension interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5269-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5269-123">Return value</span></span>

<span data-ttu-id="d5269-124">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d5269-124">Type: **HRESULT**</span></span>

<span data-ttu-id="d5269-125">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d5269-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5269-126">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5269-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5269-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5269-127">Remarks</span></span>

<span data-ttu-id="d5269-128">Una aplicación invoca este método para crear un objeto de extensión que implementa una de las interfaces de extensión de controlador de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="d5269-128">An application invokes this method to create an extension object implementing one of the WIA 2.0 driver extension interfaces.</span></span> <span data-ttu-id="d5269-129">**IWiaItem2:: getExtension** almacena la dirección de la interfaz de extensión del objeto de extensión en el parámetro *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="d5269-129">**IWiaItem2::GetExtension** stores the address of the extension object's extension interface in the *riidExtensionInterface* parameter.</span></span> <span data-ttu-id="d5269-130">A continuación, la aplicación usa el puntero de interfaz para llamar a sus métodos.</span><span class="sxs-lookup"><span data-stu-id="d5269-130">The application then uses the interface pointer to call its methods.</span></span>

<span data-ttu-id="d5269-131">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *riidExtensionInterface* .</span><span class="sxs-lookup"><span data-stu-id="d5269-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *riidExtensionInterface* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="d5269-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d5269-132">Examples</span></span>

<span data-ttu-id="d5269-133">CreateSegmentationFilter crea una instancia del filtro de segmentación del controlador ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) llamando a **IWiaItem2:: getExtension** en la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) pasada.</span><span class="sxs-lookup"><span data-stu-id="d5269-133">CreateSegmentationFilter creates an instance of the driver's segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) by calling **IWiaItem2::GetExtension** on the passed-in [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span>


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d5269-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5269-134">Requirements</span></span>



| <span data-ttu-id="d5269-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5269-135">Requirement</span></span> | <span data-ttu-id="d5269-136">Value</span><span class="sxs-lookup"><span data-stu-id="d5269-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5269-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5269-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d5269-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5269-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5269-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5269-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d5269-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5269-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5269-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5269-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5269-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5269-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5269-143">IDL</span><span class="sxs-lookup"><span data-stu-id="d5269-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5269-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5269-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 
