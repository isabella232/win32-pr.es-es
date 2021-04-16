---
description: El método Seek establece las posiciones de inicio y detención de la secuencia.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Método CPullPin. Seek (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671381"
---
# <a name="cpullpinseek-method"></a><span data-ttu-id="8cedd-103">CPullPin. Seek (método)</span><span class="sxs-lookup"><span data-stu-id="8cedd-103">CPullPin.Seek method</span></span>

<span data-ttu-id="8cedd-104">El `Seek` método establece las posiciones de inicio y detención de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cedd-104">The `Seek` method sets the start and stop positions of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cedd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cedd-105">Syntax</span></span>


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a><span data-ttu-id="8cedd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cedd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cedd-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="8cedd-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="8cedd-108">Especifica la posición inicial, en bytes multiplicada por 10 millones.</span><span class="sxs-lookup"><span data-stu-id="8cedd-108">Specifies the start position, in bytes multiplied by 10,000,000.</span></span>

</dd> <dt>

<span data-ttu-id="8cedd-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="8cedd-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="8cedd-110">Especifica la posición de detención, en bytes multiplicada por 10 millones.</span><span class="sxs-lookup"><span data-stu-id="8cedd-110">Specifies the stop position, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cedd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cedd-111">Return value</span></span>

<span data-ttu-id="8cedd-112">Devuelve S \_ OK si el método se ejecuta correctamente, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8cedd-112">Returns S\_OK if the method succeeds, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cedd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cedd-113">Remarks</span></span>

<span data-ttu-id="8cedd-114">Si el subproceso de trabajo se está ejecutando, el método pausa el subproceso, vacía el gráfico de filtro y reanuda el subproceso.</span><span class="sxs-lookup"><span data-stu-id="8cedd-114">If the worker thread is running, the method pauses the thread, flushes the filter graph, and resumes the thread.</span></span> <span data-ttu-id="8cedd-115">El subproceso empieza a extraer los datos de la nueva posición inicial.</span><span class="sxs-lookup"><span data-stu-id="8cedd-115">The thread begins pulling data from the new start position.</span></span> <span data-ttu-id="8cedd-116">De lo contrario, los nuevos valores de posición entrarán en vigor cada vez que se inicie el subproceso.</span><span class="sxs-lookup"><span data-stu-id="8cedd-116">Otherwise, the new position values become effective whenever the thread is started.</span></span>

<span data-ttu-id="8cedd-117">Las posiciones son relativas al inicio del origen original.</span><span class="sxs-lookup"><span data-stu-id="8cedd-117">Positions are relative to the start of the original source.</span></span> <span data-ttu-id="8cedd-118">Multiplique los desplazamientos de bytes deseados por las unidades constantes, que se define en la biblioteca de clases base como 10 millones.</span><span class="sxs-lookup"><span data-stu-id="8cedd-118">Multiply the desired byte offsets by the constant UNITS, which is defined in the base class library as 10,000,000.</span></span>

<span data-ttu-id="8cedd-119">Cuando el PIN se conecta por primera vez, las posiciones de detención e inicio tienen como valor predeterminado el principio y el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8cedd-119">When the pin first connects, the stop and start positions default to the beginning and end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cedd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cedd-120">Requirements</span></span>



| <span data-ttu-id="8cedd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cedd-121">Requirement</span></span> | <span data-ttu-id="8cedd-122">Value</span><span class="sxs-lookup"><span data-stu-id="8cedd-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cedd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cedd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8cedd-124"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cedd-124"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="8cedd-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cedd-125">Library</span></span><br/> | <dl> <span data-ttu-id="8cedd-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8cedd-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cedd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cedd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cedd-128">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="8cedd-128">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




