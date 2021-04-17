---
description: El método GetEncryptionKey obtiene la clave de cifrado.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'ITConnection:: GetEncryptionKey (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690203"
---
# <a name="itconnectiongetencryptionkey-method"></a><span data-ttu-id="a83f9-103">ITConnection:: GetEncryptionKey (método)</span><span class="sxs-lookup"><span data-stu-id="a83f9-103">ITConnection::GetEncryptionKey method</span></span>

<span data-ttu-id="a83f9-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a83f9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a83f9-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a83f9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a83f9-106">El método **GetEncryptionKey** obtiene la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="a83f9-106">The **GetEncryptionKey** method gets the encryption key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a83f9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a83f9-107">Syntax</span></span>


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="a83f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a83f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a83f9-109">*ppKeyType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a83f9-109">*ppKeyType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a83f9-110">Puntero a un **BSTR** que contiene el tipo de clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="a83f9-110">Pointer to a **BSTR** containing the type of encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="a83f9-111">*pfValidKeyData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a83f9-111">*pfValidKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a83f9-112">Indica la validez de los datos de claves de cifrado.</span><span class="sxs-lookup"><span data-stu-id="a83f9-112">Indicates validity of encryption key data.</span></span>

</dd> <dt>

<span data-ttu-id="a83f9-113">*ppKeyData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a83f9-113">*ppKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a83f9-114">Puntero a un **BSTR** que contiene los datos de la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="a83f9-114">Pointer to a **BSTR** containing the encryption key data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a83f9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a83f9-115">Return value</span></span>

<span data-ttu-id="a83f9-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a83f9-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a83f9-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a83f9-117">Return code</span></span>                                                                                   | <span data-ttu-id="a83f9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a83f9-118">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a83f9-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a83f9-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a83f9-120">Method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="a83f9-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a83f9-122">El parámetro *ppKeyType, pfValidKeyData* o *ppKeyData* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="a83f9-122">The *ppKeyType, pfValidKeyData,* or *ppKeyData* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a83f9-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a83f9-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a83f9-124">Insufficient memory exists to perform the operation.</span></span><br/>                              |
| <dl> <span data-ttu-id="a83f9-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a83f9-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a83f9-126">Unspecified error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a83f9-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a83f9-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="a83f9-128">This method is not yet implemented.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="a83f9-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a83f9-129">Remarks</span></span>

<span data-ttu-id="a83f9-130">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para los parámetros *ppKeyType* y *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="a83f9-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppKeyType* and *ppKeyData* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a83f9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a83f9-131">Requirements</span></span>



| <span data-ttu-id="a83f9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a83f9-132">Requirement</span></span> | <span data-ttu-id="a83f9-133">Value</span><span class="sxs-lookup"><span data-stu-id="a83f9-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a83f9-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a83f9-134">TAPI version</span></span><br/> | <span data-ttu-id="a83f9-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a83f9-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a83f9-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a83f9-136">Header</span></span><br/>       | <dl> <span data-ttu-id="a83f9-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a83f9-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a83f9-138">Library</span></span><br/>      | <dl> <span data-ttu-id="a83f9-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a83f9-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a83f9-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="a83f9-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a83f9-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a83f9-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="a83f9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83f9-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="a83f9-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

