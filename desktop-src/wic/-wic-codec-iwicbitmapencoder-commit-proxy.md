---
description: Función de proxy para el método commit.
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: IWICBitmapEncoder_Commit_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0cd3cfbe5e1c80d82cd90303d26f2da33cf467d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082089"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="9f874-103">IWICBitmapEncoder \_ función de proxy de confirmación \_</span><span class="sxs-lookup"><span data-stu-id="9f874-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="9f874-104">Función de proxy para el método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="9f874-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f874-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f874-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="9f874-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f874-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f874-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9f874-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f874-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="9f874-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="9f874-109">Puntero a este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="9f874-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f874-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f874-110">Return value</span></span>

<span data-ttu-id="9f874-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9f874-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9f874-112">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9f874-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f874-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f874-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f874-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f874-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9f874-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f874-115">Requirements</span></span>



| <span data-ttu-id="9f874-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f874-116">Requirement</span></span> | <span data-ttu-id="9f874-117">Value</span><span class="sxs-lookup"><span data-stu-id="9f874-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f874-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f874-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9f874-119">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f874-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9f874-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f874-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9f874-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f874-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9f874-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f874-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f874-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f874-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




