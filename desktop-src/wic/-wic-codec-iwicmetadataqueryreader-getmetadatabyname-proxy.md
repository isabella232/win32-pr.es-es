---
description: Función de proxy para el método GetMetadataByName.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: IWICMetadataQueryReader_GetMetadataByName_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716639"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a><span data-ttu-id="2d962-103">IWICMetadataQueryReader \_ GetMetadataByName \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="2d962-103">IWICMetadataQueryReader\_GetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="2d962-104">Función de proxy para el método [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="2d962-104">Proxy function for the [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d962-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d962-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="2d962-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d962-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d962-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2d962-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d962-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="2d962-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="2d962-109">Puntero a este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="2d962-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="2d962-110">*wzName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d962-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d962-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2d962-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="2d962-112">Nombre del elemento de metadatos solicitado.</span><span class="sxs-lookup"><span data-stu-id="2d962-112">The name of the requested metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="2d962-113">*pvarValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2d962-113">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d962-114">Tipo: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="2d962-114">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="2d962-115">Puntero que recibe la propiedad de metadatos.</span><span class="sxs-lookup"><span data-stu-id="2d962-115">Pointer that receives the metadata property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d962-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d962-116">Return value</span></span>

<span data-ttu-id="2d962-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2d962-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2d962-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2d962-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d962-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d962-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d962-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d962-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2d962-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d962-121">Requirements</span></span>



| <span data-ttu-id="2d962-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d962-122">Requirement</span></span> | <span data-ttu-id="2d962-123">Value</span><span class="sxs-lookup"><span data-stu-id="2d962-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d962-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d962-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2d962-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d962-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2d962-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d962-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2d962-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d962-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2d962-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d962-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d962-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d962-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

