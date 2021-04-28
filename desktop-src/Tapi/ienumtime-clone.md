---
description: 'Método IEnumTime::Clone: el método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.'
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: Método IEnumTime::Clone (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406dac1fad611ee5d3cb6c8b6ef32dfdb62cc963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090743"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="e4632-103">IEnumTime::Clone (método)</span><span class="sxs-lookup"><span data-stu-id="e4632-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="e4632-104">\[ Los controles e interfaces de Conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e4632-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e4632-105">La API de cliente RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e4632-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e4632-106">El **método Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="e4632-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4632-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4632-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="e4632-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4632-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4632-109">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e4632-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4632-110">Puntero al nuevo [**objeto IEnumTime.**](ienumtime.md)</span><span class="sxs-lookup"><span data-stu-id="e4632-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4632-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4632-111">Return value</span></span>

<span data-ttu-id="e4632-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e4632-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e4632-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e4632-113">Value</span></span>                                                                                         | <span data-ttu-id="e4632-114">Significado</span><span class="sxs-lookup"><span data-stu-id="e4632-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e4632-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e4632-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4632-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e4632-117"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e4632-118">El *parámetro ppEnum* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="e4632-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="e4632-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e4632-120">No existe memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e4632-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e4632-121"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="e4632-122">Error por motivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="e4632-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="e4632-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4632-123">Remarks</span></span>

<span data-ttu-id="e4632-124">TAPI llama al **método AddRef** en la [**interfaz IEnumTime**](ienumtime.md) devuelta por **IEnumTime::Clone**.</span><span class="sxs-lookup"><span data-stu-id="e4632-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="e4632-125">La aplicación debe llamar **a Release** en la **interfaz IEnumTime** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="e4632-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4632-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4632-126">Requirements</span></span>



| <span data-ttu-id="e4632-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4632-127">Requirement</span></span> | <span data-ttu-id="e4632-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e4632-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4632-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e4632-129">TAPI version</span></span><br/> | <span data-ttu-id="e4632-130">Requiere TAPI 3.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e4632-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e4632-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4632-131">Header</span></span><br/>       | <dl> <span data-ttu-id="e4632-132"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4632-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4632-133">Library</span></span><br/>      | <dl> <span data-ttu-id="e4632-134"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e4632-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e4632-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="e4632-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4632-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4632-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4632-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="e4632-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




