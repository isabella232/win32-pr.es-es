---
description: Función de proxy para el método GetFriendlyName.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706683"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a><span data-ttu-id="270f7-103">IWICComponentInfo \_ GetFriendlyName \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="270f7-103">IWICComponentInfo\_GetFriendlyName\_Proxy function</span></span>

<span data-ttu-id="270f7-104">Función de proxy para el método [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .</span><span class="sxs-lookup"><span data-stu-id="270f7-104">Proxy function for the [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="270f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="270f7-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="270f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="270f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270f7-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="270f7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270f7-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="270f7-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="270f7-109">Puntero a este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="270f7-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="270f7-110">*cchFriendlyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="270f7-110">*cchFriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="270f7-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="270f7-111">Type: **UINT**</span></span>

<span data-ttu-id="270f7-112">Tamaño del búfer de *wzFriendlyName* .</span><span class="sxs-lookup"><span data-stu-id="270f7-112">The size of the *wzFriendlyName* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="270f7-113">*wzFriendlyName* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="270f7-113">*wzFriendlyName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="270f7-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="270f7-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="270f7-115">Puntero que recibe el nombre descriptivo del componente.</span><span class="sxs-lookup"><span data-stu-id="270f7-115">A pointer that receives the friendly name of the component.</span></span>

<span data-ttu-id="270f7-116">La cadena devuelta es específica de la configuración regional, 1033 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="270f7-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="270f7-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="270f7-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="270f7-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="270f7-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="270f7-119">Puntero que recibe la longitud real del nombre descriptivo del componente.</span><span class="sxs-lookup"><span data-stu-id="270f7-119">A pointer that receives the actual length of the component's friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270f7-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="270f7-120">Return value</span></span>

<span data-ttu-id="270f7-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="270f7-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="270f7-122">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="270f7-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="270f7-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="270f7-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="270f7-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="270f7-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="270f7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="270f7-125">Requirements</span></span>



| <span data-ttu-id="270f7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="270f7-126">Requirement</span></span> | <span data-ttu-id="270f7-127">Value</span><span class="sxs-lookup"><span data-stu-id="270f7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="270f7-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="270f7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="270f7-129">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="270f7-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="270f7-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="270f7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="270f7-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="270f7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="270f7-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="270f7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="270f7-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="270f7-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




