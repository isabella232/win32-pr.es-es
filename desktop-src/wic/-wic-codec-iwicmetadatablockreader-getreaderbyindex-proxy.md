---
description: Función de proxy para el método GetReaderByIndex.
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: IWICMetadataBlockReader_GetReaderByIndex_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e2fc967f810b9ac8e43ad7da543bb1723500da48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649197"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a><span data-ttu-id="e570f-103">\_Función de proxy GetReaderByIndex de IWICMetadataBlockReader \_</span><span class="sxs-lookup"><span data-stu-id="e570f-103">IWICMetadataBlockReader\_GetReaderByIndex\_Proxy function</span></span>

<span data-ttu-id="e570f-104">Función de proxy para el método [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) .</span><span class="sxs-lookup"><span data-stu-id="e570f-104">Proxy function for the [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e570f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e570f-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a><span data-ttu-id="e570f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e570f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e570f-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e570f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e570f-108">Tipo: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="e570f-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="e570f-109">Puntero a este objeto [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="e570f-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="e570f-110">*NINDEX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e570f-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e570f-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e570f-111">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="e570f-112">*ppIMetadataReader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e570f-112">*ppIMetadataReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e570f-113">Tipo: **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span><span class="sxs-lookup"><span data-stu-id="e570f-113">Type: **[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e570f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e570f-114">Return value</span></span>

<span data-ttu-id="e570f-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e570f-115">Type: **HRESULT**</span></span>

<span data-ttu-id="e570f-116">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e570f-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e570f-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e570f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e570f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e570f-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e570f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e570f-119">Requirements</span></span>



| <span data-ttu-id="e570f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e570f-120">Requirement</span></span> | <span data-ttu-id="e570f-121">Value</span><span class="sxs-lookup"><span data-stu-id="e570f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e570f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e570f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e570f-123">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e570f-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e570f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e570f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e570f-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e570f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e570f-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e570f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e570f-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e570f-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




