---
description: Obsoleto. Use AMovieDllRegisterServer2 en su lugar.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Función AMovieDllRegisterServer (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690628"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="308b2-104">AMovieDllRegisterServer función)</span><span class="sxs-lookup"><span data-stu-id="308b2-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="308b2-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="308b2-105">Obsolete.</span></span> <span data-ttu-id="308b2-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="308b2-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="308b2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="308b2-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="308b2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="308b2-108">Parameters</span></span>

<span data-ttu-id="308b2-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="308b2-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="308b2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="308b2-110">Return value</span></span>

<span data-ttu-id="308b2-111">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="308b2-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="308b2-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="308b2-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="308b2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="308b2-113">Requirements</span></span>



| <span data-ttu-id="308b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="308b2-114">Requirement</span></span> | <span data-ttu-id="308b2-115">Value</span><span class="sxs-lookup"><span data-stu-id="308b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308b2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="308b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="308b2-117"><dt>Dllsetup. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="308b2-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="308b2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="308b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="308b2-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="308b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="308b2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="308b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="308b2-121">**Funciones de instalación de DLL**</span><span class="sxs-lookup"><span data-stu-id="308b2-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




