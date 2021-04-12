---
description: Función de proxy para el método GetCount.
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: IWICMetadataBlockReader_GetCount_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278325"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a><span data-ttu-id="d9d79-103">IWICMetadataBlockReader \_ GetCount ( \_ función de proxy)</span><span class="sxs-lookup"><span data-stu-id="d9d79-103">IWICMetadataBlockReader\_GetCount\_Proxy function</span></span>

<span data-ttu-id="d9d79-104">Función de proxy para el método [**getCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) .</span><span class="sxs-lookup"><span data-stu-id="d9d79-104">Proxy function for the [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9d79-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="d9d79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9d79-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-108">Tipo: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="d9d79-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="d9d79-109">Puntero a este objeto [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="d9d79-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="d9d79-110">*pcCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d79-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="d9d79-111">Type: \**UINT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9d79-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9d79-112">Return value</span></span>

<span data-ttu-id="d9d79-113">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d9d79-113">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d9d79-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d9d79-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9d79-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9d79-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d79-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9d79-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d79-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9d79-117">Requirements</span></span>



| <span data-ttu-id="d9d79-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9d79-118">Requirement</span></span> | <span data-ttu-id="d9d79-119">Value</span><span class="sxs-lookup"><span data-stu-id="d9d79-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d79-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9d79-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d79-121">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d9d79-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9d79-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d79-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9d79-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d9d79-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9d79-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9d79-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9d79-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




