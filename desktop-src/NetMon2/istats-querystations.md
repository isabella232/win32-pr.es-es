---
description: El método QueryStations proporciona una lista de todos los equipos que están capturando datos mediante Monitor de red.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: 'IStas:: QueryStations (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 99c3be3926191c27ad038034373e411b5c22d9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083090"
---
# <a name="istatsquerystations-method"></a><span data-ttu-id="0c799-103">IStas:: QueryStations (método)</span><span class="sxs-lookup"><span data-stu-id="0c799-103">IStats::QueryStations method</span></span>

<span data-ttu-id="0c799-104">El método **QueryStations** proporciona una lista de todos los equipos que están capturando datos mediante monitor de red.</span><span class="sxs-lookup"><span data-stu-id="0c799-104">The **QueryStations** method provides a list of all computers who are currently capturing data using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c799-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c799-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="0c799-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c799-107">*lpQueryTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0c799-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c799-108">Puntero a una estructura de [QUERYTABLE](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="0c799-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="0c799-109">En la entrada, esta estructura debe contener el número máximo de equipos que desea que devuelva Monitor de red y una matriz de estructuras [STATIONQUERY](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="0c799-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="0c799-110">En la salida, esta estructura devuelve el número de equipos que capturan datos y una estructura [STATIONQUERY](stationquery.md) para cada equipo encontrado.</span><span class="sxs-lookup"><span data-stu-id="0c799-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="0c799-111">Tenga en cuenta que esta información puede incluir equipos con versiones de Monitor de red esa versión previa 2,0.</span><span class="sxs-lookup"><span data-stu-id="0c799-111">Note that this information may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c799-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c799-112">Return value</span></span>

<span data-ttu-id="0c799-113">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0c799-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0c799-114">Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:</span><span class="sxs-lookup"><span data-stu-id="0c799-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="0c799-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0c799-115">Return code</span></span>                                                                                           | <span data-ttu-id="0c799-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c799-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c799-117"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="0c799-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="0c799-118">La memoria necesaria para procesar esta consulta no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="0c799-118">The memory required to process this query was unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c799-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c799-119">Remarks</span></span>

<span data-ttu-id="0c799-120">Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="0c799-120">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="0c799-121">Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse como Monitor de red espera a que los equipos remotos respondan a la consulta.</span><span class="sxs-lookup"><span data-stu-id="0c799-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="0c799-122">Solo se pueden consultar los equipos de la subred local.</span><span class="sxs-lookup"><span data-stu-id="0c799-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="0c799-123">Es su responsabilidad asignar la memoria para [la estructura de la tabla de](querytable.md) paginación y liberar esa memoria después de que la tabla ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="0c799-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="0c799-124">Este requisito incluye la memoria necesaria para la matriz [STATIONQUERY](stationquery.md) utilizada en la tabla de cambios.</span><span class="sxs-lookup"><span data-stu-id="0c799-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c799-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c799-125">Requirements</span></span>



| <span data-ttu-id="0c799-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c799-126">Requirement</span></span> | <span data-ttu-id="0c799-127">Value</span><span class="sxs-lookup"><span data-stu-id="0c799-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c799-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c799-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0c799-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c799-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0c799-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c799-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0c799-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c799-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0c799-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c799-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c799-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c799-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0c799-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c799-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c799-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c799-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c799-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c799-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c799-137">IStas</span><span class="sxs-lookup"><span data-stu-id="0c799-137">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="0c799-138">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="0c799-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="0c799-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="0c799-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




