---
description: El \_ método get Count obtiene el número de medios de la sesión.
ms.assetid: 9d085a34-9a49-4447-8d11-56d71a2a3592
title: 'Método ITMediaCollection:: get_Count (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f5a4fb6d7f1b942f37aae1356c7b49e0e60f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680628"
---
# <a name="itmediacollectionget_count-method"></a><span data-ttu-id="71289-103">ITMediaCollection:: get \_ Count (método)</span><span class="sxs-lookup"><span data-stu-id="71289-103">ITMediaCollection::get\_Count method</span></span>

<span data-ttu-id="71289-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71289-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71289-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="71289-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71289-106">El método **Get \_ Count** obtiene el número de medios de la sesión.</span><span class="sxs-lookup"><span data-stu-id="71289-106">The **get\_Count** method gets the number of media in the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="71289-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71289-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="71289-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71289-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71289-109">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="71289-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71289-110">Recuento de medios en la sesión.</span><span class="sxs-lookup"><span data-stu-id="71289-110">Count of media in the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71289-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71289-111">Return value</span></span>

<span data-ttu-id="71289-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="71289-112">This method can return one of these values.</span></span>



| <span data-ttu-id="71289-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="71289-113">Return code</span></span>                                                                                   | <span data-ttu-id="71289-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="71289-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="71289-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="71289-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="71289-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="71289-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71289-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="71289-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="71289-118">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="71289-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="71289-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="71289-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="71289-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="71289-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="71289-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="71289-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="71289-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="71289-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="71289-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="71289-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="71289-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="71289-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="71289-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71289-125">Requirements</span></span>



| <span data-ttu-id="71289-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="71289-126">Requirement</span></span> | <span data-ttu-id="71289-127">Value</span><span class="sxs-lookup"><span data-stu-id="71289-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71289-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="71289-128">TAPI version</span></span><br/> | <span data-ttu-id="71289-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="71289-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="71289-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71289-130">Header</span></span><br/>       | <dl> <span data-ttu-id="71289-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="71289-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="71289-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71289-132">Library</span></span><br/>      | <dl> <span data-ttu-id="71289-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71289-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="71289-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71289-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="71289-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71289-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71289-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="71289-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71289-137">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="71289-137">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




