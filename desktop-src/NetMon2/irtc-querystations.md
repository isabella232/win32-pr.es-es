---
description: Proporciona una lista de todos los equipos que usan actualmente Monitor de red para capturar datos de red.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'IRTC:: QueryStations (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001599"
---
# <a name="irtcquerystations-method"></a><span data-ttu-id="94120-103">IRTC:: QueryStations (método)</span><span class="sxs-lookup"><span data-stu-id="94120-103">IRTC::QueryStations method</span></span>

<span data-ttu-id="94120-104">El método **QueryStations** proporciona una lista de todos los equipos que usan actualmente monitor de red para capturar datos de red.</span><span class="sxs-lookup"><span data-stu-id="94120-104">The **QueryStations** method provides a list of all computers currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="94120-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94120-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="94120-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94120-107">*lpQueryTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="94120-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="94120-108">Puntero a una estructura de [**QUERYTABLE**](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="94120-108">A pointer to a [**QUERYTABLE**](querytable.md) structure.</span></span> <span data-ttu-id="94120-109">En la entrada, esta estructura debe contener el número máximo de equipos que desea que devuelva Monitor de red y una matriz de estructuras [**STATIONQUERY**](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="94120-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [**STATIONQUERY**](stationquery.md) structures.</span></span>

<span data-ttu-id="94120-110">En la salida, esta estructura devuelve el número de equipos que capturan datos y una estructura [**STATIONQUERY**](stationquery.md) para cada equipo encontrado.</span><span class="sxs-lookup"><span data-stu-id="94120-110">On output, this structure returns the number of computers capturing data and a [**STATIONQUERY**](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="94120-111">Tenga en cuenta que esto puede incluir equipos con versiones de Monitor de red esa versión de fecha 2,0.</span><span class="sxs-lookup"><span data-stu-id="94120-111">Be aware that this may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94120-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94120-112">Return value</span></span>

<span data-ttu-id="94120-113">Si el método se realiza correctamente, el valor devuelto es **NMERR \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="94120-113">If the method is successful, the return value is **NMERR\_SUCCESS**.</span></span>

<span data-ttu-id="94120-114">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="94120-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="94120-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="94120-115">Return code</span></span>                                                                                           | <span data-ttu-id="94120-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="94120-116">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="94120-117"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="94120-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="94120-118">La memoria necesaria para procesar esta consulta no está disponible.</span><span class="sxs-lookup"><span data-stu-id="94120-118">The memory required to process this query is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="94120-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94120-119">Remarks</span></span>

<span data-ttu-id="94120-120">Se puede llamar a este método en cualquier momento después de llamar al método [**CreateNPPInterface**](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="94120-120">This method can be called at any time after the [**CreateNPPInterface**](createnppinterface.md) method is called.</span></span> <span data-ttu-id="94120-121">Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse mientras Monitor de red espera a que los equipos remotos respondan a la consulta.</span><span class="sxs-lookup"><span data-stu-id="94120-121">A call to this method is a synchronous call, which may take several seconds to complete while Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="94120-122">Solo se pueden consultar los equipos de la subred local.</span><span class="sxs-lookup"><span data-stu-id="94120-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="94120-123">El usuario debe [**asignar la memoria para la estructura de**](querytable.md) la tabla de paginación y liberar esa memoria después de que ya no se necesite la tabla.</span><span class="sxs-lookup"><span data-stu-id="94120-123">The user must allocate the memory for the [**QUERYTABLE**](querytable.md) structure and free that memory after the table is no longer required.</span></span> <span data-ttu-id="94120-124">Este requisito incluye la memoria necesaria para la matriz de [**STATIONQUERY**](stationquery.md) que se usa en **QUERYTABLE**.</span><span class="sxs-lookup"><span data-stu-id="94120-124">This requirement includes memory needed for the [**STATIONQUERY**](stationquery.md) array used in **QUERYTABLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="94120-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94120-125">Requirements</span></span>



| <span data-ttu-id="94120-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="94120-126">Requirement</span></span> | <span data-ttu-id="94120-127">Value</span><span class="sxs-lookup"><span data-stu-id="94120-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94120-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94120-128">Minimum supported client</span></span><br/> | <span data-ttu-id="94120-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="94120-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="94120-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94120-130">Minimum supported server</span></span><br/> | <span data-ttu-id="94120-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94120-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="94120-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94120-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="94120-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="94120-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="94120-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94120-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94120-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94120-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94120-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="94120-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94120-137">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="94120-137">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="94120-138">**QUERYTABLE**</span><span class="sxs-lookup"><span data-stu-id="94120-138">**QUERYTABLE**</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="94120-139">**STATIONQUERY**</span><span class="sxs-lookup"><span data-stu-id="94120-139">**STATIONQUERY**</span></span>](stationquery.md)
</dt> </dl>

 

 




