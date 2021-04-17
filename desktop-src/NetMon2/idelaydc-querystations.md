---
description: El método QueryStations proporciona una lista de todos los equipos que usan actualmente Monitor de red para capturar datos.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: 'IDelaydC:: QueryStations (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5a45f5046dbd2e5714424baf42621e0c1d5539ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686565"
---
# <a name="idelaydcquerystations-method"></a><span data-ttu-id="90129-103">IDelaydC:: QueryStations (método)</span><span class="sxs-lookup"><span data-stu-id="90129-103">IDelaydC::QueryStations method</span></span>

<span data-ttu-id="90129-104">El método **QueryStations** proporciona una lista de todos los equipos que usan actualmente monitor de red para capturar datos.</span><span class="sxs-lookup"><span data-stu-id="90129-104">The **QueryStations** method provides a list of all computers that are currently using Network Monitor to capture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="90129-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90129-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="90129-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90129-107">*lpQueryTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="90129-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="90129-108">Puntero a una estructura de [QUERYTABLE](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="90129-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="90129-109">En la entrada, esta estructura debe contener el número máximo de equipos que desea que devuelva Monitor de red y una matriz de estructuras [STATIONQUERY](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="90129-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="90129-110">En la salida, esta estructura devuelve el número de equipos que capturan datos y una estructura [STATIONQUERY](stationquery.md) para cada equipo encontrado.</span><span class="sxs-lookup"><span data-stu-id="90129-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="90129-111">Tenga en cuenta que esta lista puede incluir equipos con versiones de Monitor de red esa versión previa 2,0.</span><span class="sxs-lookup"><span data-stu-id="90129-111">Note that this list might include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90129-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90129-112">Return value</span></span>

<span data-ttu-id="90129-113">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="90129-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="90129-114">Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:</span><span class="sxs-lookup"><span data-stu-id="90129-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="90129-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="90129-115">Return code</span></span>                                                                                           | <span data-ttu-id="90129-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="90129-116">Description</span></span>                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="90129-117"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="90129-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="90129-118">No había memoria disponible para procesar esta consulta.</span><span class="sxs-lookup"><span data-stu-id="90129-118">No memory was available to process this query.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90129-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90129-119">Remarks</span></span>

<span data-ttu-id="90129-120">Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="90129-120">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="90129-121">Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse como Monitor de red espera a que los equipos remotos respondan a la consulta.</span><span class="sxs-lookup"><span data-stu-id="90129-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="90129-122">Solo se pueden consultar los equipos de la subred local.</span><span class="sxs-lookup"><span data-stu-id="90129-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="90129-123">Es su responsabilidad asignar la memoria para [la estructura de la tabla de](querytable.md) paginación y liberar esa memoria después de que la tabla ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="90129-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="90129-124">Este requisito incluye la memoria necesaria para la matriz [STATIONQUERY](stationquery.md) utilizada en la tabla de cambios.</span><span class="sxs-lookup"><span data-stu-id="90129-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="90129-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90129-125">Requirements</span></span>



| <span data-ttu-id="90129-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="90129-126">Requirement</span></span> | <span data-ttu-id="90129-127">Value</span><span class="sxs-lookup"><span data-stu-id="90129-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90129-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90129-128">Minimum supported client</span></span><br/> | <span data-ttu-id="90129-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90129-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="90129-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90129-130">Minimum supported server</span></span><br/> | <span data-ttu-id="90129-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90129-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="90129-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90129-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="90129-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="90129-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="90129-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90129-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90129-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90129-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90129-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="90129-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90129-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="90129-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="90129-138">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="90129-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="90129-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="90129-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




