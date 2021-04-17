---
description: Función de proxy para el método GetDataPointer.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697813"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a><span data-ttu-id="2e673-103">IWICBitmapLock \_ GetDataPointer \_ STA \_ proxy (función)</span><span class="sxs-lookup"><span data-stu-id="2e673-103">IWICBitmapLock\_GetDataPointer\_STA\_Proxy function</span></span>

<span data-ttu-id="2e673-104">Función de proxy para el método [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .</span><span class="sxs-lookup"><span data-stu-id="2e673-104">Proxy function for the [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e673-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e673-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a><span data-ttu-id="2e673-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e673-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2e673-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e673-108">Tipo: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="2e673-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="2e673-109">Puntero a este objeto [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="2e673-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e673-110">*pcbBufferSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e673-110">*pcbBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e673-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="2e673-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="2e673-112">Puntero que recibe el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="2e673-112">A pointer that receives the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2e673-113">_ppbData \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e673-113">_ppbData\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e673-114">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="2e673-114">Type: **BYTE\*\***</span></span>

<span data-ttu-id="2e673-115">Puntero que recibe un puntero al píxel superior izquierdo del rectángulo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="2e673-115">A pointer that receives a pointer to the top left pixel in the locked rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e673-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e673-116">Return value</span></span>

<span data-ttu-id="2e673-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e673-117">Type: **HRESULT**</span></span>

<span data-ttu-id="2e673-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2e673-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e673-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e673-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e673-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e673-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2e673-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e673-121">Requirements</span></span>



| <span data-ttu-id="2e673-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e673-122">Requirement</span></span> | <span data-ttu-id="2e673-123">Value</span><span class="sxs-lookup"><span data-stu-id="2e673-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e673-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e673-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2e673-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e673-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2e673-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e673-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2e673-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e673-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2e673-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e673-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e673-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e673-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




