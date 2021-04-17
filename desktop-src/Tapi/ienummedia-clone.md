---
description: El método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'IEnumMedia:: Clone (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29671819db202643506cbdf90a1550abb305718
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691012"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="0d068-103">IEnumMedia:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="0d068-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="0d068-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0d068-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0d068-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0d068-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0d068-106">El método **Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="0d068-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d068-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d068-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="0d068-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d068-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d068-109">*ppEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d068-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d068-110">Puntero al nuevo objeto [**IEnumMedia**](ienummedia.md) .</span><span class="sxs-lookup"><span data-stu-id="0d068-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d068-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d068-111">Return value</span></span>

<span data-ttu-id="0d068-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0d068-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0d068-113">Value</span><span class="sxs-lookup"><span data-stu-id="0d068-113">Value</span></span>                                                                                         | <span data-ttu-id="0d068-114">Significado</span><span class="sxs-lookup"><span data-stu-id="0d068-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0d068-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0d068-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0d068-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d068-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d068-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0d068-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0d068-118">El parámetro *ppEnum* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="0d068-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="0d068-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d068-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0d068-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0d068-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0d068-121"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0d068-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="0d068-122">Error por razones desconocidas.</span><span class="sxs-lookup"><span data-stu-id="0d068-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="0d068-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d068-123">Remarks</span></span>

<span data-ttu-id="0d068-124">TAPI llama al método **AddRef** en la interfaz [**IEnumMedia**](ienummedia.md) devuelta por **IEnumMedia:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="0d068-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="0d068-125">La aplicación debe llamar a **Release** en la interfaz **IEnumMedia** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="0d068-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d068-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d068-126">Requirements</span></span>



| <span data-ttu-id="0d068-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d068-127">Requirement</span></span> | <span data-ttu-id="0d068-128">Value</span><span class="sxs-lookup"><span data-stu-id="0d068-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d068-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0d068-129">TAPI version</span></span><br/> | <span data-ttu-id="0d068-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0d068-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0d068-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d068-131">Header</span></span><br/>       | <dl> <span data-ttu-id="0d068-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d068-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d068-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d068-133">Library</span></span><br/>      | <dl> <span data-ttu-id="0d068-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d068-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0d068-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d068-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="0d068-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d068-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d068-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d068-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d068-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="0d068-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




