---
description: Función de proxy para el método GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717214"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a><span data-ttu-id="8ba20-103">IWICComponentInfo \_ GetVersion \_ proxy (función)</span><span class="sxs-lookup"><span data-stu-id="8ba20-103">IWICComponentInfo\_GetVersion\_Proxy function</span></span>

<span data-ttu-id="8ba20-104">Función de proxy para el método [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .</span><span class="sxs-lookup"><span data-stu-id="8ba20-104">Proxy function for the [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba20-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ba20-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="8ba20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ba20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba20-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8ba20-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba20-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8ba20-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="8ba20-109">Puntero a este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="8ba20-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="8ba20-110">*cchVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ba20-110">*cchVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba20-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8ba20-111">Type: **UINT**</span></span>

<span data-ttu-id="8ba20-112">Tamaño del búfer de *wzVersion* .</span><span class="sxs-lookup"><span data-stu-id="8ba20-112">The size of the *wzVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8ba20-113">*wzVersion* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ba20-113">*wzVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba20-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8ba20-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="8ba20-115">Puntero que recibe una cadena de referencia cultural invariable de la versión del componente.</span><span class="sxs-lookup"><span data-stu-id="8ba20-115">A pointer that receives a culture invariant string of the component's version.</span></span>

</dd> <dt>

<span data-ttu-id="8ba20-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ba20-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba20-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="8ba20-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="8ba20-118">Puntero que recibe la longitud real de la versión del componente.</span><span class="sxs-lookup"><span data-stu-id="8ba20-118">A pointer that receives the actual length of the component's version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba20-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ba20-119">Return value</span></span>

<span data-ttu-id="8ba20-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8ba20-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8ba20-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8ba20-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ba20-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ba20-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba20-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ba20-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba20-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba20-124">Requirements</span></span>



| <span data-ttu-id="8ba20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba20-125">Requirement</span></span> | <span data-ttu-id="8ba20-126">Value</span><span class="sxs-lookup"><span data-stu-id="8ba20-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba20-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba20-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba20-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ba20-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8ba20-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba20-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba20-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ba20-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8ba20-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ba20-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ba20-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ba20-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




