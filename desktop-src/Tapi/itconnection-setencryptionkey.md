---
description: El método SetEncryptionKey establece la clave de cifrado necesaria para descifrar la sesión o una indicación de un mecanismo para obtener una clave utilizable de forma externa.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'ITConnection:: SetEncryptionKey (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690197"
---
# <a name="itconnectionsetencryptionkey-method"></a><span data-ttu-id="43d2e-103">ITConnection:: SetEncryptionKey (método)</span><span class="sxs-lookup"><span data-stu-id="43d2e-103">ITConnection::SetEncryptionKey method</span></span>

<span data-ttu-id="43d2e-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="43d2e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43d2e-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="43d2e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="43d2e-106">El método **SetEncryptionKey** establece la clave de cifrado necesaria para descifrar la sesión o una indicación de un mecanismo para obtener una clave utilizable de forma externa.</span><span class="sxs-lookup"><span data-stu-id="43d2e-106">The **SetEncryptionKey** method sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d2e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43d2e-107">Syntax</span></span>


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="43d2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43d2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d2e-109">*pKeyType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43d2e-109">*pKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d2e-110">Puntero a un **BSTR** que contiene el tipo de clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="43d2e-110">Pointer to a **BSTR** containing the encryption key type.</span></span>

</dd> <dt>

<span data-ttu-id="43d2e-111">*ppKeyData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43d2e-111">*ppKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d2e-112">Puntero a un **BSTR** que contiene información de la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="43d2e-112">Pointer to a **BSTR** containing encryption key information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d2e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43d2e-113">Return value</span></span>

<span data-ttu-id="43d2e-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="43d2e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="43d2e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="43d2e-115">Return code</span></span>                                                                          | <span data-ttu-id="43d2e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="43d2e-116">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="43d2e-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="43d2e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="43d2e-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="43d2e-118">Method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43d2e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43d2e-119">Remarks</span></span>

<span data-ttu-id="43d2e-120">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para los parámetros *pKeyType* y *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="43d2e-120">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pKeyType* and *ppKeyData* parameters.</span></span> <span data-ttu-id="43d2e-121">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando las variables ya no se necesiten.</span><span class="sxs-lookup"><span data-stu-id="43d2e-121">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d2e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43d2e-122">Requirements</span></span>



| <span data-ttu-id="43d2e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="43d2e-123">Requirement</span></span> | <span data-ttu-id="43d2e-124">Value</span><span class="sxs-lookup"><span data-stu-id="43d2e-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43d2e-125">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="43d2e-125">TAPI version</span></span><br/> | <span data-ttu-id="43d2e-126">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="43d2e-126">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="43d2e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43d2e-127">Header</span></span><br/>       | <dl> <span data-ttu-id="43d2e-128"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="43d2e-128"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="43d2e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43d2e-129">Library</span></span><br/>      | <dl> <span data-ttu-id="43d2e-130"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43d2e-130"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="43d2e-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="43d2e-131">DLL</span></span><br/>          | <dl> <span data-ttu-id="43d2e-132"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43d2e-132"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d2e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="43d2e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d2e-134">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="43d2e-134">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

