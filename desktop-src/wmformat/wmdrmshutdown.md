---
title: Función WMDRMShutdown (wmdrmsdk. h)
description: La función WMDRMShutdown libera los recursos utilizados por las API extendidas del cliente DRM de Windows Media.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Función WMDRMShutdown formato de Windows Media
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678985"
---
# <a name="wmdrmshutdown-function"></a><span data-ttu-id="06906-104">WMDRMShutdown función)</span><span class="sxs-lookup"><span data-stu-id="06906-104">WMDRMShutdown function</span></span>

<span data-ttu-id="06906-105">La función **WMDRMShutdown** libera los recursos utilizados por las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="06906-105">The **WMDRMShutdown** function releases resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="06906-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06906-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a><span data-ttu-id="06906-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06906-107">Parameters</span></span>

<span data-ttu-id="06906-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="06906-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06906-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06906-109">Return value</span></span>

<span data-ttu-id="06906-110">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="06906-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="06906-111">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="06906-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="06906-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="06906-112">Return code</span></span>                                                                          | <span data-ttu-id="06906-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="06906-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="06906-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="06906-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="06906-115">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="06906-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06906-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06906-116">Remarks</span></span>

<span data-ttu-id="06906-117">Para evitar pérdidas de memoria, debe llamar a esta función para cada llamada de la función [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="06906-117">To avoid memory leaks, you must call this function for every call of the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06906-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06906-118">Requirements</span></span>



| <span data-ttu-id="06906-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06906-119">Requirement</span></span> | <span data-ttu-id="06906-120">Value</span><span class="sxs-lookup"><span data-stu-id="06906-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06906-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06906-121">Header</span></span><br/>  | <dl> <span data-ttu-id="06906-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="06906-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="06906-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06906-123">Library</span></span><br/> | <dl> <span data-ttu-id="06906-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06906-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="06906-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06906-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="06906-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06906-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06906-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="06906-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06906-128">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="06906-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





