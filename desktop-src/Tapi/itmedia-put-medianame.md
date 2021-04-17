---
description: El \_ método put MEDIANAME establece el nombre del medio. Los elementos multimedia definidos son audio, vídeo, pizarra, texto y datos.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: 'ITMedia: método de ut_MediaName de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679341"
---
# <a name="itmediaput_medianame-method"></a><span data-ttu-id="02cdb-104">ITMedia::p UT \_ medianad (método)</span><span class="sxs-lookup"><span data-stu-id="02cdb-104">ITMedia::put\_MediaName method</span></span>

<span data-ttu-id="02cdb-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="02cdb-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="02cdb-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="02cdb-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="02cdb-107">El método **Put \_ MEDIANAME** establece el nombre del medio.</span><span class="sxs-lookup"><span data-stu-id="02cdb-107">The **put\_MediaName** method sets the media name.</span></span> <span data-ttu-id="02cdb-108">Los elementos multimedia definidos son audio, vídeo, pizarra, texto y datos.</span><span class="sxs-lookup"><span data-stu-id="02cdb-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cdb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02cdb-109">Syntax</span></span>


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="02cdb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02cdb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02cdb-111">*pMediaName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02cdb-111">*pMediaName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02cdb-112">Puntero a un **BSTR** que contiene el nombre del medio que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="02cdb-112">Pointer to a **BSTR** containing the media name to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02cdb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02cdb-113">Return value</span></span>

<span data-ttu-id="02cdb-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="02cdb-114">This method can return one of these values.</span></span>



| <span data-ttu-id="02cdb-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="02cdb-115">Return code</span></span>                                                                                   | <span data-ttu-id="02cdb-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="02cdb-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="02cdb-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="02cdb-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="02cdb-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="02cdb-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="02cdb-120">El parámetro *pMediaName* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="02cdb-120">The *pMediaName* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="02cdb-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="02cdb-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="02cdb-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="02cdb-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="02cdb-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="02cdb-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="02cdb-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="02cdb-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="02cdb-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="02cdb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02cdb-127">Remarks</span></span>

<span data-ttu-id="02cdb-128">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PMediaName* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="02cdb-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="02cdb-129">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="02cdb-129">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="02cdb-130">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="02cdb-130">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02cdb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02cdb-131">Requirements</span></span>



| <span data-ttu-id="02cdb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="02cdb-132">Requirement</span></span> | <span data-ttu-id="02cdb-133">Value</span><span class="sxs-lookup"><span data-stu-id="02cdb-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02cdb-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="02cdb-134">TAPI version</span></span><br/> | <span data-ttu-id="02cdb-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="02cdb-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="02cdb-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02cdb-136">Header</span></span><br/>       | <dl> <span data-ttu-id="02cdb-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="02cdb-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02cdb-138">Library</span></span><br/>      | <dl> <span data-ttu-id="02cdb-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="02cdb-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02cdb-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="02cdb-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02cdb-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02cdb-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="02cdb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02cdb-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="02cdb-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="02cdb-144">**ITMedia:: get \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="02cdb-144">**ITMedia::get\_MediaName**</span></span>](itmedia-get-medianame.md)
</dt> </dl>

 

