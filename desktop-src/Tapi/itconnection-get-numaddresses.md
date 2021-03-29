---
description: El \_ método get NumAddresses obtiene el número de direcciones que se van a usar para la sesión.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'Método ITConnection:: get_NumAddresses (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679322"
---
# <a name="itconnectionget_numaddresses-method"></a><span data-ttu-id="16f37-103">ITConnection:: get \_ NumAddresses (método)</span><span class="sxs-lookup"><span data-stu-id="16f37-103">ITConnection::get\_NumAddresses method</span></span>

<span data-ttu-id="16f37-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="16f37-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="16f37-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="16f37-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="16f37-106">El método **Get \_ NumAddresses** obtiene el número de direcciones que se van a usar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="16f37-106">The **get\_NumAddresses** method gets the number of addresses to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f37-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16f37-107">Syntax</span></span>


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="16f37-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16f37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f37-109">*pNumAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="16f37-109">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16f37-110">Número de direcciones de la sesión.</span><span class="sxs-lookup"><span data-stu-id="16f37-110">Number of addresses for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f37-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16f37-111">Return value</span></span>

<span data-ttu-id="16f37-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="16f37-112">This method can return one of these values.</span></span>



| <span data-ttu-id="16f37-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="16f37-113">Return code</span></span>                                                                                   | <span data-ttu-id="16f37-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="16f37-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="16f37-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="16f37-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="16f37-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="16f37-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="16f37-118">El parámetro *pNumAddresse* s no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="16f37-118">The *pNumAddresse* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="16f37-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="16f37-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="16f37-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="16f37-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="16f37-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="16f37-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="16f37-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="16f37-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="16f37-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="16f37-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16f37-125">Requirements</span></span>



| <span data-ttu-id="16f37-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="16f37-126">Requirement</span></span> | <span data-ttu-id="16f37-127">Value</span><span class="sxs-lookup"><span data-stu-id="16f37-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16f37-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="16f37-128">TAPI version</span></span><br/> | <span data-ttu-id="16f37-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="16f37-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="16f37-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16f37-130">Header</span></span><br/>       | <dl> <span data-ttu-id="16f37-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="16f37-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16f37-132">Library</span></span><br/>      | <dl> <span data-ttu-id="16f37-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="16f37-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16f37-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="16f37-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f37-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f37-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="16f37-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f37-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="16f37-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




