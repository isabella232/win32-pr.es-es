---
description: El método SetConferenceBlob confirma los cambios en el BLOB de la Conferencia. Para inicializar el BLOB de la Conferencia por primera vez, utilice en su lugar el método init.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'ITConferenceBlob:: SetConferenceBlob (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680205"
---
# <a name="itconferenceblobsetconferenceblob-method"></a><span data-ttu-id="44347-104">ITConferenceBlob:: SetConferenceBlob (método)</span><span class="sxs-lookup"><span data-stu-id="44347-104">ITConferenceBlob::SetConferenceBlob method</span></span>

<span data-ttu-id="44347-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="44347-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="44347-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="44347-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="44347-107">El método **SetConferenceBlob** confirma los cambios en el BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="44347-107">The **SetConferenceBlob** method commits changes to the conference blob.</span></span> <span data-ttu-id="44347-108">Para inicializar el BLOB de la Conferencia por primera vez, utilice en su lugar el método [**init**](itconferenceblob-init.md) .</span><span class="sxs-lookup"><span data-stu-id="44347-108">To initialize the conference blob for the first time, use the [**Init**](itconferenceblob-init.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="44347-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44347-109">Syntax</span></span>


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="44347-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44347-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44347-111">*CharacterSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44347-111">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44347-112">[**BLOB \_ de \_**](blob-character-set.md) Descriptor del juego de caracteres del juego de caracteres del BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="44347-112">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the conference blob's character set.</span></span>

</dd> <dt>

<span data-ttu-id="44347-113">*pBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44347-113">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44347-114">Puntero a un **BSTR** que contiene el BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="44347-114">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44347-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44347-115">Return value</span></span>

<span data-ttu-id="44347-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="44347-116">This method can return one of these values.</span></span>



| <span data-ttu-id="44347-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="44347-117">Return code</span></span>                                                                                   | <span data-ttu-id="44347-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="44347-118">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="44347-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="44347-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="44347-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="44347-120">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="44347-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="44347-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="44347-122">El parámetro *characterSet* o *pBlob* no es válido.</span><span class="sxs-lookup"><span data-stu-id="44347-122">The *CharacterSet* or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="44347-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="44347-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="44347-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="44347-124">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="44347-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="44347-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="44347-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="44347-126">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="44347-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="44347-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="44347-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="44347-128">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="44347-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44347-129">Remarks</span></span>

<span data-ttu-id="44347-130">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PBlob* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="44347-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pBlob* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="44347-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44347-131">Requirements</span></span>



| <span data-ttu-id="44347-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="44347-132">Requirement</span></span> | <span data-ttu-id="44347-133">Value</span><span class="sxs-lookup"><span data-stu-id="44347-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44347-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="44347-134">TAPI version</span></span><br/> | <span data-ttu-id="44347-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="44347-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="44347-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44347-136">Header</span></span><br/>       | <dl> <span data-ttu-id="44347-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="44347-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="44347-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44347-138">Library</span></span><br/>      | <dl> <span data-ttu-id="44347-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44347-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="44347-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44347-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="44347-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44347-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44347-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="44347-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44347-143">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="44347-143">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="44347-144">**\_juego de caracteres de blob \_**</span><span class="sxs-lookup"><span data-stu-id="44347-144">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

