---
description: Función de proxy para el método GetStride.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: IWICBitmapLock_GetStride_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706953"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a><span data-ttu-id="07838-103">IWICBitmapLock \_ GetStride \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="07838-103">IWICBitmapLock\_GetStride\_Proxy function</span></span>

<span data-ttu-id="07838-104">Función de proxy para el método [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) .</span><span class="sxs-lookup"><span data-stu-id="07838-104">Proxy function for the [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07838-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07838-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a><span data-ttu-id="07838-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07838-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="07838-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07838-108">Tipo: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="07838-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="07838-109">Puntero a este objeto [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="07838-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="07838-110">*pcbStride* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="07838-110">*pcbStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07838-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="07838-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="07838-112">El intervalo del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="07838-112">The bitmap stride.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07838-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07838-113">Return value</span></span>

<span data-ttu-id="07838-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="07838-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="07838-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="07838-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07838-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07838-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="07838-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07838-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="07838-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07838-118">Requirements</span></span>



| <span data-ttu-id="07838-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="07838-119">Requirement</span></span> | <span data-ttu-id="07838-120">Value</span><span class="sxs-lookup"><span data-stu-id="07838-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07838-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07838-121">Minimum supported client</span></span><br/> | <span data-ttu-id="07838-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07838-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="07838-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07838-123">Minimum supported server</span></span><br/> | <span data-ttu-id="07838-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="07838-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="07838-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07838-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07838-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07838-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




