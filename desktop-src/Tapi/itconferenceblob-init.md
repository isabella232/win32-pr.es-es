---
description: El método init inicializa el BLOB de la Conferencia en función de una cadena de texto. Si pBlob es NULL, se usan los valores predeterminados.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'ITConferenceBlob:: init (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690441"
---
# <a name="itconferenceblobinit-method"></a><span data-ttu-id="76793-104">ITConferenceBlob:: init (método)</span><span class="sxs-lookup"><span data-stu-id="76793-104">ITConferenceBlob::Init method</span></span>

<span data-ttu-id="76793-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="76793-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="76793-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="76793-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="76793-107">El método **init** inicializa el BLOB de la Conferencia en función de una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="76793-107">The **Init** method initializes the conference blob based on a textual string.</span></span> <span data-ttu-id="76793-108">Si *pBlob* es **null**, se usan los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="76793-108">If *pBlob* is **NULL**, default values are used.</span></span>

## <a name="syntax"></a><span data-ttu-id="76793-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76793-109">Syntax</span></span>


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="76793-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76793-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76793-111">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76793-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76793-112">Puntero a una representación **BSTR** del nombre de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="76793-112">Pointer to a **BSTR** representation of the conference name.</span></span>

</dd> <dt>

<span data-ttu-id="76793-113">*CharacterSet* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76793-113">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76793-114">[**BLOB \_ de Descriptor \_ del juego de caracteres del**](blob-character-set.md) juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76793-114">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> <dt>

<span data-ttu-id="76793-115">*pBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76793-115">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76793-116">Puntero a un **BSTR** que contiene el BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="76793-116">Pointer to a **BSTR** containing the conference blob.</span></span> <span data-ttu-id="76793-117">Si es **null**, el BLOB de la Conferencia se inicializa con los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="76793-117">If **NULL**, the conference blob is initialized with default values.</span></span> <span data-ttu-id="76793-118">Actualmente, los valores de conferencia predeterminados solo están disponibles si el parámetro *characterSet* está establecido en el ASCII de BCS \_ .</span><span class="sxs-lookup"><span data-stu-id="76793-118">Currently, default conference values are available only if the *CharacterSet* parameter is set to BCS\_ASCII.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76793-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76793-119">Return value</span></span>

<span data-ttu-id="76793-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="76793-120">This method can return one of these values.</span></span>



| <span data-ttu-id="76793-121">Value</span><span class="sxs-lookup"><span data-stu-id="76793-121">Value</span></span>                                                                                         | <span data-ttu-id="76793-122">Significado</span><span class="sxs-lookup"><span data-stu-id="76793-122">Meaning</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76793-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="76793-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="76793-124">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="76793-124">Method succeeded.</span></span><br/>                                               |
| <dl> <span data-ttu-id="76793-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="76793-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="76793-126">El parámetro *pName*, *characterSet* o *pBlob* no es válido.</span><span class="sxs-lookup"><span data-stu-id="76793-126">The *pName*, *CharacterSet*, or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="76793-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="76793-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="76793-128">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="76793-128">Insufficient memory exists to perform the operation.</span></span><br/>            |
| <dl> <span data-ttu-id="76793-129"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="76793-129"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="76793-130">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="76793-130">Unspecified error.</span></span><br/>                                              |
| <dl> <span data-ttu-id="76793-131"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="76793-131"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="76793-132">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="76793-132">This method is not yet implemented.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="76793-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76793-133">Remarks</span></span>

<span data-ttu-id="76793-134">**ITConferenceBlob:: init** devolverá un error si ya se ha inicializado el BLOB.</span><span class="sxs-lookup"><span data-stu-id="76793-134">**ITConferenceBlob::Init** will return a failure if the blob has already been initialized.</span></span>

<span data-ttu-id="76793-135">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para los parámetros *pName* y *pBlob* .</span><span class="sxs-lookup"><span data-stu-id="76793-135">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* and *pBlob* parameters.</span></span> <span data-ttu-id="76793-136">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando las variables ya no se necesiten.</span><span class="sxs-lookup"><span data-stu-id="76793-136">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="76793-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76793-137">Requirements</span></span>



| <span data-ttu-id="76793-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="76793-138">Requirement</span></span> | <span data-ttu-id="76793-139">Value</span><span class="sxs-lookup"><span data-stu-id="76793-139">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76793-140">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="76793-140">TAPI version</span></span><br/> | <span data-ttu-id="76793-141">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="76793-141">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="76793-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76793-142">Header</span></span><br/>       | <dl> <span data-ttu-id="76793-143"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="76793-143"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="76793-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76793-144">Library</span></span><br/>      | <dl> <span data-ttu-id="76793-145"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76793-145"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="76793-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="76793-146">DLL</span></span><br/>          | <dl> <span data-ttu-id="76793-147"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76793-147"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76793-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="76793-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76793-149">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="76793-149">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="76793-150">**\_juego de caracteres de blob \_**</span><span class="sxs-lookup"><span data-stu-id="76793-150">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

