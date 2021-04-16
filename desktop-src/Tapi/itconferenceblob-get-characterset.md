---
description: El \_ método get characterSet obtiene un \_ \_ descriptor de juego de caracteres de BLOB del juego de caracteres utilizado en el BLOB de la Conferencia actual.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Método ITConferenceBlob:: get_CharacterSet (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680208"
---
# <a name="itconferenceblobget_characterset-method"></a><span data-ttu-id="14b8f-103">ITConferenceBlob:: get \_ characterSet (método)</span><span class="sxs-lookup"><span data-stu-id="14b8f-103">ITConferenceBlob::get\_CharacterSet method</span></span>

<span data-ttu-id="14b8f-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="14b8f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14b8f-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="14b8f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="14b8f-106">El método **Get \_ characterSet** obtiene un descriptor de juego de [**\_ caracteres \_ de BLOB**](blob-character-set.md) del juego de caracteres utilizado en el BLOB de la Conferencia actual.</span><span class="sxs-lookup"><span data-stu-id="14b8f-106">The **get\_CharacterSet** method gets a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set used in the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b8f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14b8f-107">Syntax</span></span>


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a><span data-ttu-id="14b8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14b8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b8f-109">*pCharacterSet* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="14b8f-109">*pCharacterSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14b8f-110">Puntero a un descriptor del juego de [**\_ \_ caracteres de BLOB**](blob-character-set.md) del juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="14b8f-110">Pointer to a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b8f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14b8f-111">Return value</span></span>

<span data-ttu-id="14b8f-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="14b8f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="14b8f-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="14b8f-113">Return code</span></span>                                                                                                   | <span data-ttu-id="14b8f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="14b8f-114">Description</span></span>                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="14b8f-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-115"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="14b8f-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="14b8f-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="14b8f-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-117"><dt>**E\_POINTER**</dt></span></span> </dl>                     | <span data-ttu-id="14b8f-118">El parámetro *pCharacterSet* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="14b8f-118">The *pCharacterSet* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="14b8f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                 | <span data-ttu-id="14b8f-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="14b8f-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="14b8f-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-121"><dt>**E\_FAIL**</dt></span></span> </dl>                        | <span data-ttu-id="14b8f-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="14b8f-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="14b8f-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                     | <span data-ttu-id="14b8f-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="14b8f-124">This method is not yet implemented.</span></span><br/>                   |
| <dl> <span data-ttu-id="14b8f-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                  | <span data-ttu-id="14b8f-126">*pCharacterSet* es **null**.</span><span class="sxs-lookup"><span data-stu-id="14b8f-126">*pCharacterSet* is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="14b8f-127"><dt>**VALOR ERROR de \_ datos no válidos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-127"><dt>**(HRESULT) ERROR\_INVALID\_DATA**</dt></span></span> </dl> | <span data-ttu-id="14b8f-128">El juego de caracteres actual no es válido o no está disponible.</span><span class="sxs-lookup"><span data-stu-id="14b8f-128">The current character set is invalid or unavailable.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="14b8f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14b8f-129">Requirements</span></span>



| <span data-ttu-id="14b8f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b8f-130">Requirement</span></span> | <span data-ttu-id="14b8f-131">Value</span><span class="sxs-lookup"><span data-stu-id="14b8f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14b8f-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="14b8f-132">TAPI version</span></span><br/> | <span data-ttu-id="14b8f-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="14b8f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="14b8f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14b8f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="14b8f-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="14b8f-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14b8f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="14b8f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="14b8f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14b8f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="14b8f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b8f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b8f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="14b8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b8f-141">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="14b8f-141">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="14b8f-142">**\_juego de caracteres de blob \_**</span><span class="sxs-lookup"><span data-stu-id="14b8f-142">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

 




