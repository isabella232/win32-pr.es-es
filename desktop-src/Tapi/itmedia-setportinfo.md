---
description: El método SetPortInfo establece el valor de puerto de 16 bits para el primer puerto y el número de puertos necesarios para una sesión.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'ITMedia:: SetPortInfo (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690980"
---
# <a name="itmediasetportinfo-method"></a><span data-ttu-id="671d9-103">ITMedia:: SetPortInfo (método)</span><span class="sxs-lookup"><span data-stu-id="671d9-103">ITMedia::SetPortInfo method</span></span>

<span data-ttu-id="671d9-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="671d9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="671d9-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="671d9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="671d9-106">El método **SetPortInfo** establece el valor de puerto de 16 bits para el primer puerto y el número de puertos necesarios para una sesión.</span><span class="sxs-lookup"><span data-stu-id="671d9-106">The **SetPortInfo** method sets the 16-bit port value for the first port and the number of ports needed for a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="671d9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="671d9-107">Syntax</span></span>


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="671d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="671d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671d9-109">*StartPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="671d9-109">*StartPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671d9-110">Puerto de inicio.</span><span class="sxs-lookup"><span data-stu-id="671d9-110">Starting port.</span></span> <span data-ttu-id="671d9-111">Puede ser un valor comprendido en el intervalo de 0-65535.</span><span class="sxs-lookup"><span data-stu-id="671d9-111">This can be a value in the range 0-65535.</span></span>

</dd> <dt>

<span data-ttu-id="671d9-112">*NumPorts* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="671d9-112">*NumPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671d9-113">Número de puertos.</span><span class="sxs-lookup"><span data-stu-id="671d9-113">Number of ports.</span></span> <span data-ttu-id="671d9-114">Puede ser un valor comprendido en el intervalo de 0-65535.</span><span class="sxs-lookup"><span data-stu-id="671d9-114">This can be a value in the range 0-65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671d9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="671d9-115">Return value</span></span>

<span data-ttu-id="671d9-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="671d9-116">This method can return one of these values.</span></span>



| <span data-ttu-id="671d9-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="671d9-117">Return code</span></span>                                                                                   | <span data-ttu-id="671d9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="671d9-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="671d9-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="671d9-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="671d9-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="671d9-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="671d9-122">El parámetro *StartPort o NumPorts* no es válido.</span><span class="sxs-lookup"><span data-stu-id="671d9-122">The *StartPort or NumPorts* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="671d9-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="671d9-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="671d9-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="671d9-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="671d9-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="671d9-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="671d9-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="671d9-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="671d9-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="671d9-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="671d9-129">Remarks</span></span>

<span data-ttu-id="671d9-130">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="671d9-130">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="671d9-131">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="671d9-131">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="671d9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671d9-132">Requirements</span></span>



| <span data-ttu-id="671d9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="671d9-133">Requirement</span></span> | <span data-ttu-id="671d9-134">Value</span><span class="sxs-lookup"><span data-stu-id="671d9-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="671d9-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="671d9-135">TAPI version</span></span><br/> | <span data-ttu-id="671d9-136">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="671d9-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="671d9-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="671d9-137">Header</span></span><br/>       | <dl> <span data-ttu-id="671d9-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="671d9-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="671d9-139">Library</span></span><br/>      | <dl> <span data-ttu-id="671d9-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="671d9-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="671d9-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="671d9-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="671d9-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671d9-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="671d9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671d9-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="671d9-144">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




