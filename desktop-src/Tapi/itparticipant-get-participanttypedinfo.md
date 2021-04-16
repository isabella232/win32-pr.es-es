---
description: El \_ método get ParticipantTypedInfo obtiene una representación BSTR del tipo de información necesaria, como PTI \_ EmailAddress.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Método ITParticipant:: get_ParticipantTypedInfo (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679155"
---
# <a name="itparticipantget_participanttypedinfo-method"></a><span data-ttu-id="eb4bb-103">ITParticipant:: get \_ ParticipantTypedInfo (método)</span><span class="sxs-lookup"><span data-stu-id="eb4bb-103">ITParticipant::get\_ParticipantTypedInfo method</span></span>

<span data-ttu-id="eb4bb-104">\[**obtener \_ ParticipantTypedInfo** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-104">\[**get\_ParticipantTypedInfo** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eb4bb-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="eb4bb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="eb4bb-106">El método **Get \_ ParticipantTypedInfo** obtiene una representación **BSTR** del tipo de información necesaria, como PTI \_ EmailAddress.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-106">The **get\_ParticipantTypedInfo** method gets a **BSTR** representation of the type of information needed, such as PTI\_EMAILADDRESS.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb4bb-107">Syntax</span></span>


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="eb4bb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb4bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4bb-109">*InfoType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eb4bb-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4bb-110">[**Participante \_ Descriptor de \_ información con tipo**](participant-typed-info.md) del tipo de información necesaria.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-110">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) descriptor of the type of information needed.</span></span>

</dd> <dt>

<span data-ttu-id="eb4bb-111">*ppInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eb4bb-111">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4bb-112">Puntero a la representación **BSTR** de la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-112">Pointer to **BSTR** representation of the information needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4bb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb4bb-113">Return value</span></span>

<span data-ttu-id="eb4bb-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-114">This method can return one of these values.</span></span>



| <span data-ttu-id="eb4bb-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="eb4bb-115">Return code</span></span>                                                                                    | <span data-ttu-id="eb4bb-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb4bb-116">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="eb4bb-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="eb4bb-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="eb4bb-119"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-119"><dt>**E\_FAIL**</dt></span></span> </dl>         | <span data-ttu-id="eb4bb-120">No se pudo almacenar la información en *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="eb4bb-120">Storage of information into *ppInfo* failed.</span></span><br/>         |
| <dl> <span data-ttu-id="eb4bb-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="eb4bb-122">El parámetro *InfoType* no es válido.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-122">The *InfoType* parameter is not valid.</span></span><br/>               |
| <dl> <span data-ttu-id="eb4bb-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-123"><dt>**E\_POINTER**</dt></span></span> </dl>      | <span data-ttu-id="eb4bb-124">El parámetro *ppInfo* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-124">The *ppInfo* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="eb4bb-125"><dt>**TAPI \_ E \_ noitem**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-125"><dt>**TAPI\_E\_NOITEM**</dt></span></span> </dl> | <span data-ttu-id="eb4bb-126">TAPI no tiene información sobre el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-126">TAPI has no information on the specified type.</span></span><br/>       |
| <dl> <span data-ttu-id="eb4bb-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>  | <span data-ttu-id="eb4bb-128">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="eb4bb-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb4bb-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb4bb-129">Remarks</span></span>

<span data-ttu-id="eb4bb-130">La aplicación debe usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="eb4bb-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4bb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb4bb-131">Requirements</span></span>



| <span data-ttu-id="eb4bb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb4bb-132">Requirement</span></span> | <span data-ttu-id="eb4bb-133">Value</span><span class="sxs-lookup"><span data-stu-id="eb4bb-133">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4bb-134">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="eb4bb-134">TAPI version</span></span><br/> | <span data-ttu-id="eb4bb-135">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="eb4bb-135">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="eb4bb-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb4bb-136">Header</span></span><br/>       | <dl> <span data-ttu-id="eb4bb-137"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-137"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb4bb-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb4bb-138">Library</span></span><br/>      | <dl> <span data-ttu-id="eb4bb-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-139"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="eb4bb-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb4bb-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="eb4bb-141"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb4bb-141"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb4bb-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb4bb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4bb-143">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="eb4bb-143">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="eb4bb-144">**\_información con tipo de participante \_**</span><span class="sxs-lookup"><span data-stu-id="eb4bb-144">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> <dt>

[<span data-ttu-id="eb4bb-145">**tipos de medios**</span><span class="sxs-lookup"><span data-stu-id="eb4bb-145">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

