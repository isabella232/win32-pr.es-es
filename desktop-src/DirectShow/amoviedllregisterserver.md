---
description: 'Función AMovieDllRegisterServer: obsoleta. Use AMovieDllRegisterServer2 en su lugar.'
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Función AMovieDllRegisterServer (Dllsetup.h)
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
ms.openlocfilehash: 81b6e73b1988d3eb97abdf9a5d2415ecbd62d8c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099943"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="d9e32-104">Función AMovieDllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="d9e32-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="d9e32-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d9e32-105">Obsolete.</span></span> <span data-ttu-id="d9e32-106">Use [**AMovieDllRegisterServer2 en**](amoviedllregisterserver2.md) su lugar.</span><span class="sxs-lookup"><span data-stu-id="d9e32-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e32-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9e32-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="d9e32-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9e32-108">Parameters</span></span>

<span data-ttu-id="d9e32-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d9e32-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9e32-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9e32-110">Return value</span></span>

<span data-ttu-id="d9e32-111">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d9e32-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9e32-112">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d9e32-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e32-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9e32-113">Requirements</span></span>



| <span data-ttu-id="d9e32-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9e32-114">Requirement</span></span> | <span data-ttu-id="d9e32-115">Value</span><span class="sxs-lookup"><span data-stu-id="d9e32-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e32-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9e32-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d9e32-117"><dt>Dllsetup.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9e32-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d9e32-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9e32-118">Library</span></span><br/> | <dl> <span data-ttu-id="d9e32-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d9e32-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9e32-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d9e32-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e32-121">**Funciones de instalación de DLL**</span><span class="sxs-lookup"><span data-stu-id="d9e32-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




