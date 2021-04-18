---
description: Función de proxy para el método GetAuthor.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707002"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a><span data-ttu-id="ff0e5-103">IWICComponentInfo \_ GetAuthor \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="ff0e5-103">IWICComponentInfo\_GetAuthor\_Proxy function</span></span>

<span data-ttu-id="ff0e5-104">Función de proxy para el método [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) .</span><span class="sxs-lookup"><span data-stu-id="ff0e5-104">Proxy function for the [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff0e5-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="ff0e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff0e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff0e5-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ff0e5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0e5-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="ff0e5-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="ff0e5-109">Puntero a este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="ff0e5-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="ff0e5-110">*cchAuthor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff0e5-110">*cchAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0e5-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ff0e5-111">Type: **UINT**</span></span>

<span data-ttu-id="ff0e5-112">Tamaño del búfer de *wzAuthor* .</span><span class="sxs-lookup"><span data-stu-id="ff0e5-112">The size of the *wzAuthor* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ff0e5-113">*wzAuthor* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ff0e5-113">*wzAuthor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0e5-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="ff0e5-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="ff0e5-115">Puntero que recibe el nombre del autor del componente.</span><span class="sxs-lookup"><span data-stu-id="ff0e5-115">A pointer that receives the name of the component's author.</span></span>

<span data-ttu-id="ff0e5-116">La cadena devuelta es específica de la configuración regional, 1033 de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ff0e5-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="ff0e5-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ff0e5-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0e5-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="ff0e5-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="ff0e5-119">Puntero que recibe la longitud real del nombre de los autores del componente.</span><span class="sxs-lookup"><span data-stu-id="ff0e5-119">A pointer that receives the actual length of the component's authors name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff0e5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff0e5-120">Return value</span></span>

<span data-ttu-id="ff0e5-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ff0e5-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ff0e5-122">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ff0e5-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff0e5-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff0e5-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff0e5-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff0e5-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0e5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff0e5-125">Requirements</span></span>



| <span data-ttu-id="ff0e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff0e5-126">Requirement</span></span> | <span data-ttu-id="ff0e5-127">Value</span><span class="sxs-lookup"><span data-stu-id="ff0e5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0e5-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff0e5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0e5-129">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff0e5-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ff0e5-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff0e5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0e5-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff0e5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ff0e5-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff0e5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff0e5-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff0e5-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




