---
description: El método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'IEnumTime:: Clone (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681000"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="54509-103">IEnumTime:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="54509-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="54509-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="54509-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="54509-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="54509-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="54509-106">El método **Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="54509-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="54509-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54509-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="54509-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54509-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54509-109">*ppEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54509-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54509-110">Puntero al nuevo objeto [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="54509-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54509-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54509-111">Return value</span></span>

<span data-ttu-id="54509-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="54509-112">This method can return one of these values.</span></span>



| <span data-ttu-id="54509-113">Value</span><span class="sxs-lookup"><span data-stu-id="54509-113">Value</span></span>                                                                                         | <span data-ttu-id="54509-114">Significado</span><span class="sxs-lookup"><span data-stu-id="54509-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="54509-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="54509-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="54509-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="54509-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="54509-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="54509-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="54509-118">El parámetro *ppEnum* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="54509-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="54509-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="54509-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="54509-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="54509-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="54509-121"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="54509-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="54509-122">Error por razones desconocidas.</span><span class="sxs-lookup"><span data-stu-id="54509-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="54509-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54509-123">Remarks</span></span>

<span data-ttu-id="54509-124">TAPI llama al método **AddRef** en la interfaz [**IEnumTime**](ienumtime.md) devuelta por **IEnumTime:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="54509-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="54509-125">La aplicación debe llamar a **Release** en la interfaz **IEnumTime** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="54509-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="54509-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54509-126">Requirements</span></span>



| <span data-ttu-id="54509-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="54509-127">Requirement</span></span> | <span data-ttu-id="54509-128">Value</span><span class="sxs-lookup"><span data-stu-id="54509-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54509-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="54509-129">TAPI version</span></span><br/> | <span data-ttu-id="54509-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="54509-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="54509-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54509-131">Header</span></span><br/>       | <dl> <span data-ttu-id="54509-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="54509-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="54509-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54509-133">Library</span></span><br/>      | <dl> <span data-ttu-id="54509-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54509-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="54509-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54509-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="54509-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54509-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54509-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="54509-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54509-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="54509-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




