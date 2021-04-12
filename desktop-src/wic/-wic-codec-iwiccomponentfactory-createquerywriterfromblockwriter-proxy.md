---
description: Función de proxy para el método CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278193"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a><span data-ttu-id="4bed9-103">IWICComponentFactory \_ CreateQueryWriterFromBlockWriter \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="4bed9-103">IWICComponentFactory\_CreateQueryWriterFromBlockWriter\_Proxy function</span></span>

<span data-ttu-id="4bed9-104">Función de proxy para el método [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) .</span><span class="sxs-lookup"><span data-stu-id="4bed9-104">Proxy function for the [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bed9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bed9-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="4bed9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bed9-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bed9-108">Tipo: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="4bed9-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="4bed9-109">Puntero a este objeto [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="4bed9-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="4bed9-110">*pIBlockWriter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-110">*pIBlockWriter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bed9-111">Tipo: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _</span><span class="sxs-lookup"><span data-stu-id="4bed9-111">Type: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\** _</span></span>

</dd> <dt>

<span data-ttu-id="4bed9-112">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-112">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bed9-113">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="4bed9-113">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bed9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bed9-114">Return value</span></span>

<span data-ttu-id="4bed9-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4bed9-115">Type: **HRESULT**</span></span>

<span data-ttu-id="4bed9-116">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4bed9-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bed9-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4bed9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bed9-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bed9-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4bed9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bed9-119">Requirements</span></span>



| <span data-ttu-id="4bed9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bed9-120">Requirement</span></span> | <span data-ttu-id="4bed9-121">Value</span><span class="sxs-lookup"><span data-stu-id="4bed9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bed9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bed9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4bed9-123">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4bed9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bed9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4bed9-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bed9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4bed9-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bed9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bed9-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bed9-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




