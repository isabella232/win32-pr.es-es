---
description: Función de proxy para el método GetCLSID.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: IWICComponentInfo_GetCLSID_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc63d3f30605c0f5343502bcb96e989cc8496540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707419"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a><span data-ttu-id="bece9-103">IWICComponentInfo \_ GetCLSID \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="bece9-103">IWICComponentInfo\_GetCLSID\_Proxy function</span></span>

<span data-ttu-id="bece9-104">Función de proxy para el método [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) .</span><span class="sxs-lookup"><span data-stu-id="bece9-104">Proxy function for the [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bece9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bece9-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a><span data-ttu-id="bece9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bece9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bece9-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="bece9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bece9-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="bece9-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="bece9-109">Puntero a este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="bece9-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="bece9-110">*pclsid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bece9-110">*pclsid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bece9-111">Tipo: \**CLSID \** _</span><span class="sxs-lookup"><span data-stu-id="bece9-111">Type: \**CLSID\** _</span></span>

<span data-ttu-id="bece9-112">Puntero que recibe el CLSID del componente.</span><span class="sxs-lookup"><span data-stu-id="bece9-112">A pointer that receives the component's CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bece9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bece9-113">Return value</span></span>

<span data-ttu-id="bece9-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="bece9-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="bece9-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bece9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bece9-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bece9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bece9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bece9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bece9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bece9-118">Requirements</span></span>



| <span data-ttu-id="bece9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bece9-119">Requirement</span></span> | <span data-ttu-id="bece9-120">Value</span><span class="sxs-lookup"><span data-stu-id="bece9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bece9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bece9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bece9-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bece9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bece9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bece9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bece9-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bece9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bece9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bece9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bece9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bece9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




