---
title: Función WMDRMStartup (wmdrmsdk. h)
description: La función WMDRMStartup inicializa los recursos usados por las API extendidas del cliente DRM de Windows Media.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Función WMDRMStartup formato de Windows Media
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649986"
---
# <a name="wmdrmstartup-function"></a><span data-ttu-id="c8b10-104">WMDRMStartup función)</span><span class="sxs-lookup"><span data-stu-id="c8b10-104">WMDRMStartup function</span></span>

<span data-ttu-id="c8b10-105">La función **WMDRMStartup** inicializa los recursos usados por las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c8b10-105">The **WMDRMStartup** function initializes resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b10-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8b10-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a><span data-ttu-id="c8b10-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8b10-107">Parameters</span></span>

<span data-ttu-id="c8b10-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c8b10-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8b10-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8b10-109">Return value</span></span>

<span data-ttu-id="c8b10-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c8b10-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c8b10-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="c8b10-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c8b10-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c8b10-112">Return code</span></span>                                                                          | <span data-ttu-id="c8b10-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8b10-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c8b10-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c8b10-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c8b10-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="c8b10-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8b10-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8b10-116">Remarks</span></span>

<span data-ttu-id="c8b10-117">Para cada llamada de esta función, debe llamar a [**WMDRMShutdown**](wmdrmshutdown.md) para liberar los recursos usados.</span><span class="sxs-lookup"><span data-stu-id="c8b10-117">For every call of this function, you must call [**WMDRMShutdown**](wmdrmshutdown.md) to release the resources used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b10-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8b10-118">Requirements</span></span>



| <span data-ttu-id="c8b10-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b10-119">Requirement</span></span> | <span data-ttu-id="c8b10-120">Value</span><span class="sxs-lookup"><span data-stu-id="c8b10-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b10-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8b10-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c8b10-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b10-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8b10-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8b10-123">Library</span></span><br/> | <dl> <span data-ttu-id="c8b10-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8b10-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8b10-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8b10-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8b10-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8b10-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b10-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8b10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b10-128">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="c8b10-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





