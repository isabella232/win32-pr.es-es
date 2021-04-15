---
description: La función LoadOLEAut32 carga la biblioteca de vínculos dinámicos de automatización (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Función LoadOLEAut32 (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690016"
---
# <a name="loadoleaut32-function"></a><span data-ttu-id="d8d4a-103">LoadOLEAut32 función)</span><span class="sxs-lookup"><span data-stu-id="d8d4a-103">LoadOLEAut32 function</span></span>

<span data-ttu-id="d8d4a-104">La función **LoadOLEAut32** carga la biblioteca de vínculos dinámicos de automatización (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="d8d4a-104">The **LoadOLEAut32** function loads the Automation dynamic-link library (OleAut32.dll).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d4a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8d4a-105">Syntax</span></span>


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a><span data-ttu-id="d8d4a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8d4a-106">Parameters</span></span>

<span data-ttu-id="d8d4a-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8d4a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8d4a-108">Return value</span></span>

<span data-ttu-id="d8d4a-109">Devuelve un identificador para una instancia de DLL de Automation.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-109">Returns a handle to an Automation DLL instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d4a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8d4a-110">Remarks</span></span>

<span data-ttu-id="d8d4a-111">Cuando el destructor [**CBaseObject**](cbaseobject.md) destruye el objeto que se cargó OleAut32.dll, descargará la biblioteca si todavía está cargada.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-111">When the [**CBaseObject**](cbaseobject.md) destructor destroys the object that loaded OleAut32.dll, it will unload the library if it is still loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d4a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8d4a-112">Requirements</span></span>



| <span data-ttu-id="d8d4a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8d4a-113">Requirement</span></span> | <span data-ttu-id="d8d4a-114">Value</span><span class="sxs-lookup"><span data-stu-id="d8d4a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d4a-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8d4a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d8d4a-116"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8d4a-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8d4a-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8d4a-117">Library</span></span><br/> | <dl> <span data-ttu-id="d8d4a-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d8d4a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d4a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8d4a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d4a-120">**Funciones auxiliares de COM**</span><span class="sxs-lookup"><span data-stu-id="d8d4a-120">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




