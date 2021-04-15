---
description: Función de proxy para el método CreateComponentInfo.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: IWICImagingFactory_CreateComponentInfo_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361171"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a><span data-ttu-id="4e318-103">IWICImagingFactory \_ CreateComponentInfo \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="4e318-103">IWICImagingFactory\_CreateComponentInfo\_Proxy function</span></span>

<span data-ttu-id="4e318-104">Función de proxy para el método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="4e318-104">Proxy function for the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e318-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e318-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e318-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e318-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e318-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e318-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="4e318-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="4e318-109">_clsidComponent \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4e318-109">_clsidComponent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e318-110">Tipo: **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="4e318-110">Type: **REFCLSID**</span></span>

<span data-ttu-id="4e318-111">CLSID del componente deseado.</span><span class="sxs-lookup"><span data-stu-id="4e318-111">The CLSID for the desired component.</span></span>

</dd> <dt>

<span data-ttu-id="4e318-112">*ppIInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4e318-112">*ppIInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e318-113">Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="4e318-113">Type: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span></span>

<span data-ttu-id="4e318-114">Puntero que recibe un puntero a un nuevo [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span><span class="sxs-lookup"><span data-stu-id="4e318-114">A pointer that receives a pointer to a new [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e318-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e318-115">Return value</span></span>

<span data-ttu-id="4e318-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4e318-116">Type: **HRESULT**</span></span>

<span data-ttu-id="4e318-117">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4e318-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e318-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e318-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e318-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e318-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4e318-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e318-120">Requirements</span></span>



| <span data-ttu-id="4e318-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e318-121">Requirement</span></span> | <span data-ttu-id="4e318-122">Value</span><span class="sxs-lookup"><span data-stu-id="4e318-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e318-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e318-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e318-124">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e318-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4e318-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e318-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e318-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e318-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4e318-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e318-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e318-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e318-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




