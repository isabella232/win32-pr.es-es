---
description: El \_ método get Count obtiene el número de elementos de la colección.
ms.assetid: 9fe96af3-bb7b-4f6c-8df2-85bf7850c527
title: 'Método ITTimeCollection:: get_Count (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a385c8fa3120cbeaa4b876a8af4f60e0df5cb48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690236"
---
# <a name="ittimecollectionget_count-method"></a><span data-ttu-id="2a37a-103">ITTimeCollection:: get \_ Count (método)</span><span class="sxs-lookup"><span data-stu-id="2a37a-103">ITTimeCollection::get\_Count method</span></span>

<span data-ttu-id="2a37a-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2a37a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2a37a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2a37a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2a37a-106">El método **Get \_ Count** obtiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="2a37a-106">The **get\_Count** method gets the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a37a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a37a-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2a37a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a37a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a37a-109">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2a37a-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a37a-110">Puntero al número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="2a37a-110">Pointer to the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a37a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a37a-111">Return value</span></span>

<span data-ttu-id="2a37a-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2a37a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2a37a-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2a37a-113">Return code</span></span>                                                                                   | <span data-ttu-id="2a37a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a37a-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2a37a-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2a37a-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a37a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2a37a-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2a37a-118">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="2a37a-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="2a37a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2a37a-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="2a37a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2a37a-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2a37a-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="2a37a-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2a37a-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2a37a-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="2a37a-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2a37a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a37a-125">Requirements</span></span>



| <span data-ttu-id="2a37a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a37a-126">Requirement</span></span> | <span data-ttu-id="2a37a-127">Value</span><span class="sxs-lookup"><span data-stu-id="2a37a-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a37a-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="2a37a-128">TAPI version</span></span><br/> | <span data-ttu-id="2a37a-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2a37a-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2a37a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a37a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="2a37a-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a37a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a37a-132">Library</span></span><br/>      | <dl> <span data-ttu-id="2a37a-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2a37a-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a37a-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="2a37a-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a37a-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a37a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a37a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a37a-137">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="2a37a-137">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="2a37a-138">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="2a37a-138">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




