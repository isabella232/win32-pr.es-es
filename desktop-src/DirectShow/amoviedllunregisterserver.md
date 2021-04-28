---
description: 'Función AMovieDllUnregisterServer: obsoleta. Use AMovieDllRegisterServer2 en su lugar.'
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Función AMovieDllUnregisterServer (Dllsetup.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099933"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="410f5-104">Función AMovieDllUnregisterServer</span><span class="sxs-lookup"><span data-stu-id="410f5-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="410f5-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="410f5-105">Obsolete.</span></span> <span data-ttu-id="410f5-106">Use [**AMovieDllRegisterServer2 en**](amoviedllregisterserver2.md) su lugar.</span><span class="sxs-lookup"><span data-stu-id="410f5-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="410f5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="410f5-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="410f5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="410f5-108">Parameters</span></span>

<span data-ttu-id="410f5-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="410f5-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="410f5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="410f5-110">Return value</span></span>

<span data-ttu-id="410f5-111">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="410f5-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="410f5-112">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="410f5-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="410f5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="410f5-113">Requirements</span></span>



| <span data-ttu-id="410f5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="410f5-114">Requirement</span></span> | <span data-ttu-id="410f5-115">Value</span><span class="sxs-lookup"><span data-stu-id="410f5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410f5-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="410f5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="410f5-117"><dt>Dllsetup.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="410f5-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="410f5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="410f5-118">Library</span></span><br/> | <dl> <span data-ttu-id="410f5-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="410f5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410f5-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="410f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410f5-121">**Funciones de instalación de DLL**</span><span class="sxs-lookup"><span data-stu-id="410f5-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




