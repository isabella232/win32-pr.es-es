---
description: El \_ método put MediaTitle establece un título textual para los medios que la aplicación puede usar con fines informativos o de presentación. Debe ser una cadena que se pueda convertir en ASCII si el juego de caracteres es ASCII. De lo contrario, puede ser cualquier cadena BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: 'ITMedia: método de ut_MediaTitle de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690176"
---
# <a name="itmediaput_mediatitle-method"></a><span data-ttu-id="fff0c-105">ITMedia::p \_ método MediaTitle UT</span><span class="sxs-lookup"><span data-stu-id="fff0c-105">ITMedia::put\_MediaTitle method</span></span>

<span data-ttu-id="fff0c-106">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fff0c-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fff0c-107">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="fff0c-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fff0c-108">El método **Put \_ MediaTitle** establece un título textual para los medios que la aplicación puede usar con fines informativos o de presentación.</span><span class="sxs-lookup"><span data-stu-id="fff0c-108">The **put\_MediaTitle** method sets a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="fff0c-109">Debe ser una cadena que se pueda convertir en ASCII si el juego de caracteres es ASCII.</span><span class="sxs-lookup"><span data-stu-id="fff0c-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="fff0c-110">De lo contrario, puede ser cualquier cadena **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="fff0c-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff0c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fff0c-111">Syntax</span></span>


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="fff0c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fff0c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff0c-113">*pMediaTitle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fff0c-113">*pMediaTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff0c-114">Puntero a un **BSTR** que contiene el título del medio.</span><span class="sxs-lookup"><span data-stu-id="fff0c-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fff0c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fff0c-115">Return value</span></span>

<span data-ttu-id="fff0c-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="fff0c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fff0c-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fff0c-117">Return code</span></span>                                                                                   | <span data-ttu-id="fff0c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fff0c-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fff0c-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fff0c-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fff0c-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fff0c-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fff0c-122">El parámetro *pMediaTitle* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="fff0c-122">The *pMediaTitle* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="fff0c-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fff0c-124">El parámetro *pMediaTitle* no es válido.</span><span class="sxs-lookup"><span data-stu-id="fff0c-124">The *pMediaTitle* parameter is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="fff0c-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fff0c-126">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="fff0c-126">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fff0c-127"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-127"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fff0c-128">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="fff0c-128">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fff0c-129"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-129"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fff0c-130">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="fff0c-130">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fff0c-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fff0c-131">Remarks</span></span>

<span data-ttu-id="fff0c-132">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PMediaTitle* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="fff0c-132">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaTitle* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="fff0c-133">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="fff0c-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="fff0c-134">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="fff0c-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff0c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fff0c-135">Requirements</span></span>



| <span data-ttu-id="fff0c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fff0c-136">Requirement</span></span> | <span data-ttu-id="fff0c-137">Value</span><span class="sxs-lookup"><span data-stu-id="fff0c-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fff0c-138">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="fff0c-138">TAPI version</span></span><br/> | <span data-ttu-id="fff0c-139">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="fff0c-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fff0c-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fff0c-140">Header</span></span><br/>       | <dl> <span data-ttu-id="fff0c-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fff0c-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fff0c-142">Library</span></span><br/>      | <dl> <span data-ttu-id="fff0c-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fff0c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fff0c-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="fff0c-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff0c-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fff0c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="fff0c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff0c-147">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="fff0c-147">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="fff0c-148">**ITMedia:: get \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="fff0c-148">**ITMedia::get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)
</dt> </dl>

 

