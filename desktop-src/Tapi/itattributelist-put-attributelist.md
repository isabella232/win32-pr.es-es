---
description: El \_ método put AttributeList establece la lista de atributos.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: 'ITAttributeList: método de ut_AttributeList de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3876b2cd8ecdef46a933ff3f3c91be96dd028892
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690924"
---
# <a name="itattributelistput_attributelist-method"></a><span data-ttu-id="ce65d-103">ITAttributeList::p el \_ método UT AttributeList</span><span class="sxs-lookup"><span data-stu-id="ce65d-103">ITAttributeList::put\_AttributeList method</span></span>

<span data-ttu-id="ce65d-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ce65d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ce65d-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ce65d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ce65d-106">El método **Put \_ AttributeList** establece la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="ce65d-106">The **put\_AttributeList** method sets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce65d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce65d-107">Syntax</span></span>


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="ce65d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce65d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce65d-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ce65d-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce65d-110">Matriz de atributos que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="ce65d-110">Array of attributes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce65d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce65d-111">Return value</span></span>

<span data-ttu-id="ce65d-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ce65d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ce65d-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ce65d-113">Return code</span></span>                                                                                   | <span data-ttu-id="ce65d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce65d-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ce65d-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ce65d-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce65d-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ce65d-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ce65d-118">El parámetro *newVal* no es válido.</span><span class="sxs-lookup"><span data-stu-id="ce65d-118">The *newVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="ce65d-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ce65d-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ce65d-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ce65d-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ce65d-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ce65d-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ce65d-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ce65d-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="ce65d-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="ce65d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce65d-125">Requirements</span></span>



| <span data-ttu-id="ce65d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce65d-126">Requirement</span></span> | <span data-ttu-id="ce65d-127">Value</span><span class="sxs-lookup"><span data-stu-id="ce65d-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce65d-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ce65d-128">TAPI version</span></span><br/> | <span data-ttu-id="ce65d-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ce65d-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ce65d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce65d-130">Header</span></span><br/>       | <dl> <span data-ttu-id="ce65d-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce65d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce65d-132">Library</span></span><br/>      | <dl> <span data-ttu-id="ce65d-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ce65d-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce65d-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="ce65d-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce65d-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce65d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce65d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce65d-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="ce65d-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="ce65d-138">**ITAttributeList:: get \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="ce65d-138">**ITAttributeList::get\_AttributeList**</span></span>](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




