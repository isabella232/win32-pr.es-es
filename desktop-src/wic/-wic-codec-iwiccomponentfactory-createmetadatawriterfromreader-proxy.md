---
description: Función de proxy para el método CreateMetadataWriterFromReader.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: IWICComponentFactory_CreateMetadataWriterFromReader_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910421"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a><span data-ttu-id="b897e-103">IWICComponentFactory \_ CreateMetadataWriterFromReader \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="b897e-103">IWICComponentFactory\_CreateMetadataWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="b897e-104">Función de proxy para el método [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="b897e-104">Proxy function for the [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b897e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b897e-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a><span data-ttu-id="b897e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b897e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b897e-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b897e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b897e-108">Tipo: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="b897e-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="b897e-109">Puntero a este objeto [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="b897e-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="b897e-110">*pIReader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b897e-110">*pIReader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b897e-111">Tipo: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _</span><span class="sxs-lookup"><span data-stu-id="b897e-111">Type: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\** _</span></span>

</dd> <dt>

<span data-ttu-id="b897e-112">_pguidVendor \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b897e-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b897e-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="b897e-113">Type: \**const GUID\** _</span></span>

</dd> <dt>

<span data-ttu-id="b897e-114">_ppIWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b897e-114">_ppIWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b897e-115">Tipo: **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="b897e-115">Type: **[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b897e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b897e-116">Return value</span></span>

<span data-ttu-id="b897e-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b897e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="b897e-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b897e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b897e-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b897e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b897e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b897e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b897e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b897e-121">Requirements</span></span>



| <span data-ttu-id="b897e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b897e-122">Requirement</span></span> | <span data-ttu-id="b897e-123">Value</span><span class="sxs-lookup"><span data-stu-id="b897e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b897e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b897e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b897e-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b897e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b897e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b897e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b897e-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b897e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b897e-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b897e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b897e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b897e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




