---
description: Función de proxy para el método GetContainerFormat.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706415"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="4c954-103">IWICMetadataQueryReader \_ GetContainerFormat \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="4c954-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="4c954-104">Función de proxy para el método [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="4c954-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c954-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c954-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="4c954-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c954-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4c954-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c954-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="4c954-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="4c954-109">Puntero a este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="4c954-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="4c954-110">*pguidContainerFormat* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4c954-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c954-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="4c954-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="4c954-112">Puntero que recibe el GUID de formato cointainer.</span><span class="sxs-lookup"><span data-stu-id="4c954-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c954-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c954-113">Return value</span></span>

<span data-ttu-id="4c954-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4c954-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4c954-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4c954-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c954-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c954-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c954-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c954-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4c954-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c954-118">Requirements</span></span>



| <span data-ttu-id="4c954-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c954-119">Requirement</span></span> | <span data-ttu-id="4c954-120">Value</span><span class="sxs-lookup"><span data-stu-id="4c954-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c954-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c954-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4c954-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c954-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4c954-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c954-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4c954-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c954-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4c954-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c954-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c954-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c954-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




