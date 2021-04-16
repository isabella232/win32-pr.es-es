---
description: El \_ método get BandwidthModifier obtiene el modificador de ancho de banda, que es una sola palabra alfanumérica que ofrece el significado de la figura de ancho de banda. Los dos modificadores definidos son CT (total de la Conferencia) y como (máximo específico de la aplicación).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'Método ITConnection:: get_BandwidthModifier (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679324"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a><span data-ttu-id="3b8c3-104">ITConnection:: get \_ BandwidthModifier (método)</span><span class="sxs-lookup"><span data-stu-id="3b8c3-104">ITConnection::get\_BandwidthModifier method</span></span>

<span data-ttu-id="3b8c3-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3b8c3-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3b8c3-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3b8c3-107">El método **Get \_ BandwidthModifier** obtiene el modificador de ancho de banda, que es una sola palabra alfanumérica que ofrece el significado de la figura de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-107">The **get\_BandwidthModifier** method gets the bandwidth modifier, which is a single, alphanumeric word giving the meaning of the bandwidth figure.</span></span> <span data-ttu-id="3b8c3-108">Los dos modificadores definidos son CT (total de la Conferencia) y como (máximo específico de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="3b8c3-108">The two modifiers defined are CT (Conference Total) and AS (Application Specific Maximum).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8c3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b8c3-109">Syntax</span></span>


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a><span data-ttu-id="3b8c3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b8c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b8c3-111">*ppModifier* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3b8c3-111">*ppModifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8c3-112">Puntero a un **BSTR** que contiene el modificador de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-112">Pointer to a **BSTR** containing the bandwidth modifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b8c3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b8c3-113">Return value</span></span>

<span data-ttu-id="3b8c3-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3b8c3-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3b8c3-115">Return code</span></span>                                                                                   | <span data-ttu-id="3b8c3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b8c3-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3b8c3-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3b8c3-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3b8c3-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3b8c3-120">El parámetro *ppModifier* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-120">The *ppModifier* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="3b8c3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3b8c3-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3b8c3-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3b8c3-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3b8c3-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3b8c3-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="3b8c3-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3b8c3-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b8c3-127">Remarks</span></span>

<span data-ttu-id="3b8c3-128">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppModifier* .</span><span class="sxs-lookup"><span data-stu-id="3b8c3-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppModifier* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8c3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b8c3-129">Requirements</span></span>



| <span data-ttu-id="3b8c3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8c3-130">Requirement</span></span> | <span data-ttu-id="3b8c3-131">Value</span><span class="sxs-lookup"><span data-stu-id="3b8c3-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8c3-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="3b8c3-132">TAPI version</span></span><br/> | <span data-ttu-id="3b8c3-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3b8c3-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3b8c3-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b8c3-134">Header</span></span><br/>       | <dl> <span data-ttu-id="3b8c3-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b8c3-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b8c3-136">Library</span></span><br/>      | <dl> <span data-ttu-id="3b8c3-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3b8c3-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b8c3-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="3b8c3-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c3-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8c3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b8c3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8c3-141">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="3b8c3-141">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

