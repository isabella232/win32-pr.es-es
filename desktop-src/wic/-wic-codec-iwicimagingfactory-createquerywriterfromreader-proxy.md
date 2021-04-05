---
description: Función de proxy para el método CreateQueryWriterFromReader.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: IWICImagingFactory_CreateQueryWriterFromReader_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002796"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a><span data-ttu-id="410d7-103">IWICImagingFactory \_ CreateQueryWriterFromReader \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="410d7-103">IWICImagingFactory\_CreateQueryWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="410d7-104">Función de proxy para el método [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="410d7-104">Proxy function for the [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="410d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="410d7-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="410d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="410d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="410d7-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="410d7-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="410d7-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="410d7-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="410d7-109">_pIQueryReader \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="410d7-109">_pIQueryReader\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="410d7-110">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="410d7-110">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="410d7-111">Lector de consultas de metadatos desde el que se va a crear el escritor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="410d7-111">The metadata query reader to create the metadata writer from.</span></span>

</dd> <dt>

<span data-ttu-id="410d7-112">_pguidVendor \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="410d7-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="410d7-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="410d7-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="410d7-114">GUID del proveedor para el escritor de consultas de metadatos.</span><span class="sxs-lookup"><span data-stu-id="410d7-114">The vendor GUID for the metadata query writer.</span></span>

</dd> <dt>

<span data-ttu-id="410d7-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="410d7-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="410d7-116">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="410d7-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="410d7-117">Puntero que recibe un puntero a un nuevo [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="410d7-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="410d7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="410d7-118">Return value</span></span>

<span data-ttu-id="410d7-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="410d7-119">Type: **HRESULT**</span></span>

<span data-ttu-id="410d7-120">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="410d7-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="410d7-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="410d7-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="410d7-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="410d7-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="410d7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="410d7-123">Requirements</span></span>



| <span data-ttu-id="410d7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="410d7-124">Requirement</span></span> | <span data-ttu-id="410d7-125">Value</span><span class="sxs-lookup"><span data-stu-id="410d7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410d7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="410d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="410d7-127">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="410d7-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="410d7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="410d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="410d7-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="410d7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="410d7-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="410d7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="410d7-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="410d7-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




