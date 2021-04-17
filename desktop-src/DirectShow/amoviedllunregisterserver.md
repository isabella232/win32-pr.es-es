---
description: Obsoleto. Use AMovieDllRegisterServer2 en su lugar.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Función AMovieDllUnregisterServer (Dllsetup. h)
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
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690799"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="42f06-104">AMovieDllUnregisterServer función)</span><span class="sxs-lookup"><span data-stu-id="42f06-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="42f06-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="42f06-105">Obsolete.</span></span> <span data-ttu-id="42f06-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="42f06-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f06-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42f06-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="42f06-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42f06-108">Parameters</span></span>

<span data-ttu-id="42f06-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="42f06-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42f06-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42f06-110">Return value</span></span>

<span data-ttu-id="42f06-111">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="42f06-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42f06-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42f06-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f06-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f06-113">Requirements</span></span>



| <span data-ttu-id="42f06-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f06-114">Requirement</span></span> | <span data-ttu-id="42f06-115">Value</span><span class="sxs-lookup"><span data-stu-id="42f06-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f06-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42f06-116">Header</span></span><br/>  | <dl> <span data-ttu-id="42f06-117"><dt>Dllsetup. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42f06-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="42f06-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42f06-118">Library</span></span><br/> | <dl> <span data-ttu-id="42f06-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="42f06-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f06-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="42f06-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f06-121">**Funciones de instalación de DLL**</span><span class="sxs-lookup"><span data-stu-id="42f06-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




