---
description: El \_ método get MEDIANAME obtiene el nombre del medio. Los elementos multimedia definidos son audio, vídeo, pizarra, texto y datos.
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'Método ITMedia:: get_MediaName (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9152994eac98d5e846ac147072a51a3334930da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690850"
---
# <a name="itmediaget_medianame-method"></a><span data-ttu-id="29332-104">ITMedia:: get \_ MEDIANAME (método)</span><span class="sxs-lookup"><span data-stu-id="29332-104">ITMedia::get\_MediaName method</span></span>

<span data-ttu-id="29332-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="29332-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="29332-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="29332-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="29332-107">El método **Get \_ MEDIANAME** obtiene el nombre del medio.</span><span class="sxs-lookup"><span data-stu-id="29332-107">The **get\_MediaName** method gets the media name.</span></span> <span data-ttu-id="29332-108">Los elementos multimedia definidos son audio, vídeo, pizarra, texto y datos.</span><span class="sxs-lookup"><span data-stu-id="29332-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="29332-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29332-109">Syntax</span></span>


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="29332-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29332-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29332-111">*ppMediaName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="29332-111">*ppMediaName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29332-112">Puntero a un **BSTR** que contiene el nombre del medio, como audio.</span><span class="sxs-lookup"><span data-stu-id="29332-112">Pointer to a **BSTR** containing the name of the media, such as audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29332-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29332-113">Return value</span></span>

<span data-ttu-id="29332-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="29332-114">This method can return one of these values.</span></span>



| <span data-ttu-id="29332-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="29332-115">Return code</span></span>                                                                                   | <span data-ttu-id="29332-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="29332-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="29332-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="29332-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="29332-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="29332-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="29332-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="29332-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="29332-120">El parámetro *ppMediaName* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="29332-120">The *ppMediaName* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="29332-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="29332-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="29332-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="29332-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="29332-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="29332-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="29332-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="29332-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="29332-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="29332-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="29332-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="29332-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="29332-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29332-127">Remarks</span></span>

<span data-ttu-id="29332-128">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppMediaName* .</span><span class="sxs-lookup"><span data-stu-id="29332-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="29332-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29332-129">Requirements</span></span>



| <span data-ttu-id="29332-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="29332-130">Requirement</span></span> | <span data-ttu-id="29332-131">Value</span><span class="sxs-lookup"><span data-stu-id="29332-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29332-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="29332-132">TAPI version</span></span><br/> | <span data-ttu-id="29332-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="29332-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="29332-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29332-134">Header</span></span><br/>       | <dl> <span data-ttu-id="29332-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="29332-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="29332-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29332-136">Library</span></span><br/>      | <dl> <span data-ttu-id="29332-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29332-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="29332-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29332-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="29332-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29332-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29332-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="29332-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29332-141">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="29332-141">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="29332-142">**ITMedia::p UT \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="29332-142">**ITMedia::put\_MediaName**</span></span>](itmedia-put-medianame.md)
</dt> </dl>

 

