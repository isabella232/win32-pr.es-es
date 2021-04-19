---
description: Función de proxy para el método GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717215"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a><span data-ttu-id="630fd-103">IWICComponentInfo \_ GetSpecVersion \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="630fd-103">IWICComponentInfo\_GetSpecVersion\_Proxy function</span></span>

<span data-ttu-id="630fd-104">Función de proxy para el método [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .</span><span class="sxs-lookup"><span data-stu-id="630fd-104">Proxy function for the [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="630fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="630fd-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="630fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="630fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="630fd-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="630fd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="630fd-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="630fd-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="630fd-109">Puntero a este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="630fd-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="630fd-110">*cchSpecVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="630fd-110">*cchSpecVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="630fd-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="630fd-111">Type: **UINT**</span></span>

<span data-ttu-id="630fd-112">Tamaño del búfer de *wzSpecVersion* .</span><span class="sxs-lookup"><span data-stu-id="630fd-112">The size of the *wzSpecVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="630fd-113">*wzSpecVersion* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="630fd-113">*wzSpecVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="630fd-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="630fd-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="630fd-115">Cuando este método devuelve un valor, contiene una cadena de invarient de referencia cultural de la versión de especificación del componente.</span><span class="sxs-lookup"><span data-stu-id="630fd-115">When this method returns, contain a culture invarient string of the component's specification version.</span></span> <span data-ttu-id="630fd-116">El formato de versión es NN. NN. NN. NN.</span><span class="sxs-lookup"><span data-stu-id="630fd-116">The version form is NN.NN.NN.NN.</span></span>

</dd> <dt>

<span data-ttu-id="630fd-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="630fd-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="630fd-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="630fd-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="630fd-119">Puntero que recibe la longitud real de la versión de especificación del componente.</span><span class="sxs-lookup"><span data-stu-id="630fd-119">A pointer that receives the actual length of the component's specification version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="630fd-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="630fd-120">Return value</span></span>

<span data-ttu-id="630fd-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="630fd-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="630fd-122">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="630fd-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="630fd-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="630fd-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="630fd-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="630fd-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="630fd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="630fd-125">Requirements</span></span>



| <span data-ttu-id="630fd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="630fd-126">Requirement</span></span> | <span data-ttu-id="630fd-127">Value</span><span class="sxs-lookup"><span data-stu-id="630fd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="630fd-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="630fd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="630fd-129">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="630fd-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="630fd-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="630fd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="630fd-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="630fd-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="630fd-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="630fd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="630fd-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="630fd-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




