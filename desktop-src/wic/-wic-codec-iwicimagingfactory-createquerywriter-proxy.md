---
description: Función de proxy para el método CreateQueryWriter.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: IWICImagingFactory_CreateQueryWriter_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817107"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a><span data-ttu-id="a56fc-103">IWICImagingFactory \_ CreateQueryWriter \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="a56fc-103">IWICImagingFactory\_CreateQueryWriter\_Proxy function</span></span>

<span data-ttu-id="a56fc-104">Función de proxy para el método [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="a56fc-104">Proxy function for the [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a56fc-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="a56fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a56fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56fc-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a56fc-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a56fc-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a56fc-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="a56fc-109">_guidMetadataFormat \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a56fc-109">_guidMetadataFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a56fc-110">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="a56fc-110">Type: **REFGUID**</span></span>

<span data-ttu-id="a56fc-111">GUID para el formato de metadatos deseado.</span><span class="sxs-lookup"><span data-stu-id="a56fc-111">The GUID for the desired metadata format.</span></span>

</dd> <dt>

<span data-ttu-id="a56fc-112">*pguidVendor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a56fc-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a56fc-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="a56fc-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="a56fc-114">GUID del proveedor del escritor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="a56fc-114">The vendor GUID of the metadata writer.</span></span>

</dd> <dt>

<span data-ttu-id="a56fc-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a56fc-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a56fc-116">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="a56fc-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="a56fc-117">Puntero que recibe un puntero a un nuevo [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="a56fc-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a56fc-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a56fc-118">Return value</span></span>

<span data-ttu-id="a56fc-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a56fc-119">Type: **HRESULT**</span></span>

<span data-ttu-id="a56fc-120">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a56fc-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a56fc-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a56fc-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a56fc-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a56fc-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a56fc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a56fc-123">Requirements</span></span>



| <span data-ttu-id="a56fc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56fc-124">Requirement</span></span> | <span data-ttu-id="a56fc-125">Value</span><span class="sxs-lookup"><span data-stu-id="a56fc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a56fc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a56fc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a56fc-127">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a56fc-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a56fc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a56fc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a56fc-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a56fc-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a56fc-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a56fc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a56fc-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a56fc-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




