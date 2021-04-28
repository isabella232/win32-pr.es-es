---
description: 'IWICFastMetadataEncoder_Commit_Proxy función: función proxy para el método Commit.'
ms.assetid: 5b3b90ad-9d67-4fbd-b01e-c7478df8dd45
title: IWICFastMetadataEncoder_Commit_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 848ed74ec9c9bb490065935bd94cae7a35d02db2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097193"
---
# <a name="iwicfastmetadataencoder_commit_proxy-function"></a><span data-ttu-id="ac1e5-103">Función IWICFastMetadataEncoder \_ Commit \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="ac1e5-103">IWICFastMetadataEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="ac1e5-104">Función de proxy para el [**método Commit.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit)</span><span class="sxs-lookup"><span data-stu-id="ac1e5-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac1e5-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_Commit_Proxy(
  _In_ IWICFastMetadataEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="ac1e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac1e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac1e5-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ac1e5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1e5-108">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span><span class="sxs-lookup"><span data-stu-id="ac1e5-108">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span></span>

<span data-ttu-id="ac1e5-109">Puntero a este [**objeto IWICFastMetadataEncoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)</span><span class="sxs-lookup"><span data-stu-id="ac1e5-109">Pointer to this [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac1e5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac1e5-110">Return value</span></span>

<span data-ttu-id="ac1e5-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac1e5-111">Type: **HRESULT**</span></span>

<span data-ttu-id="ac1e5-112">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ac1e5-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac1e5-113">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="ac1e5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac1e5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac1e5-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac1e5-115">Requirements</span></span>



| <span data-ttu-id="ac1e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac1e5-116">Requirement</span></span> | <span data-ttu-id="ac1e5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ac1e5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1e5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac1e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1e5-119">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ac1e5-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ac1e5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac1e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1e5-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac1e5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ac1e5-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac1e5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1e5-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac1e5-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




