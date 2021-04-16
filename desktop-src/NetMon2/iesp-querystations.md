---
description: El método QueryStations proporciona una lista de todos los equipos que usan actualmente Monitor de red para capturar datos de red.
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: 'IESP:: QueryStations (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5287f472b2a0641eb29e4f1b37b6fe4e089dfa86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686558"
---
# <a name="iespquerystations-method"></a><span data-ttu-id="6c5a7-103">IESP:: QueryStations (método)</span><span class="sxs-lookup"><span data-stu-id="6c5a7-103">IESP::QueryStations method</span></span>

<span data-ttu-id="6c5a7-104">El método **QueryStations** proporciona una lista de todos los equipos que usan actualmente monitor de red para capturar datos de red.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-104">The **QueryStations** method provides a list of all computers that currently use Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c5a7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="6c5a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c5a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5a7-107">*lpQueryTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c5a7-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5a7-108">Puntero a una estructura de [QUERYTABLE](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="6c5a7-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="6c5a7-109">En la entrada, esta estructura debe contener el número máximo de equipos que desea que devuelva Monitor de red y una matriz de estructuras [STATIONQUERY](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="6c5a7-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="6c5a7-110">En la salida, esta estructura devuelve el número de equipos que capturan datos y una estructura [STATIONQUERY](stationquery.md) para cada equipo encontrado.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="6c5a7-111">Tenga en cuenta que este total puede incluir equipos con versiones de Monitor de red esa versión previa 2,0.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-111">Note that this total may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5a7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c5a7-112">Return value</span></span>

<span data-ttu-id="6c5a7-113">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6c5a7-114">Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:</span><span class="sxs-lookup"><span data-stu-id="6c5a7-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="6c5a7-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6c5a7-115">Return code</span></span>                                                                                           | <span data-ttu-id="6c5a7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c5a7-116">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c5a7-117"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a7-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="6c5a7-118">La memoria necesaria para procesar esta consulta no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-118">The memory needed to process this query was unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c5a7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c5a7-119">Remarks</span></span>

<span data-ttu-id="6c5a7-120">Se puede llamar a este método en cualquier momento después de llamar al método [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="6c5a7-120">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="6c5a7-121">Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse como Monitor de red espera a que los equipos remotos respondan a la consulta.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="6c5a7-122">Solo se pueden consultar los equipos de la subred local.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="6c5a7-123">Es su responsabilidad asignar la memoria para [la estructura de la tabla de](querytable.md) paginación y liberar esa memoria después de que la tabla ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="6c5a7-124">Este requisito incluye la memoria necesaria para la matriz [STATIONQUERY](stationquery.md) utilizada en la tabla de cambios.</span><span class="sxs-lookup"><span data-stu-id="6c5a7-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5a7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c5a7-125">Requirements</span></span>



| <span data-ttu-id="6c5a7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c5a7-126">Requirement</span></span> | <span data-ttu-id="6c5a7-127">Value</span><span class="sxs-lookup"><span data-stu-id="6c5a7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5a7-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c5a7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5a7-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c5a7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6c5a7-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c5a7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5a7-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c5a7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6c5a7-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c5a7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5a7-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a7-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6c5a7-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c5a7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c5a7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5a7-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c5a7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5a7-137">IESP</span><span class="sxs-lookup"><span data-stu-id="6c5a7-137">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="6c5a7-138">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="6c5a7-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="6c5a7-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="6c5a7-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




