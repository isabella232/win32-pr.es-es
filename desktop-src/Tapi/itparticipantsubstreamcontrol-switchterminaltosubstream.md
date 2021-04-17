---
description: El método SwitchTerminalToSubStream establece un terminal en la subsecuencia del participante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'ITParticipantSubStreamControl:: SwitchTerminalToSubStream (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681241"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a><span data-ttu-id="8785c-103">ITParticipantSubStreamControl:: SwitchTerminalToSubStream (método)</span><span class="sxs-lookup"><span data-stu-id="8785c-103">ITParticipantSubStreamControl::SwitchTerminalToSubStream method</span></span>

<span data-ttu-id="8785c-104">\[**SwitchTerminalToSubStream** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8785c-104">\[**SwitchTerminalToSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8785c-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8785c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8785c-106">El método **SwitchTerminalToSubStream** establece un terminal en la subsecuencia del participante.</span><span class="sxs-lookup"><span data-stu-id="8785c-106">The **SwitchTerminalToSubStream** method sets a terminal to the participant substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8785c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8785c-107">Syntax</span></span>


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="8785c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8785c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8785c-109">*pITTerminal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8785c-109">*pITTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8785c-110">Puntero a la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="8785c-110">Pointer to [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8785c-111">*pITSubStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8785c-111">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8785c-112">Puntero a la interfaz [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="8785c-112">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8785c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8785c-113">Return value</span></span>

<span data-ttu-id="8785c-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8785c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8785c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8785c-115">Return code</span></span>                                                                                     | <span data-ttu-id="8785c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8785c-116">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8785c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="8785c-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8785c-118">Method succeeded.</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="8785c-119"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>    | <span data-ttu-id="8785c-120">No se pudo tener acceso a la información de los participantes de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8785c-120">Participant information for the stream could not be accessed.</span></span><br/>                           |
| <dl> <span data-ttu-id="8785c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="8785c-122">Los parámetros *pParticipant* o *pITSubStream* no apuntan a una interfaz válida.</span><span class="sxs-lookup"><span data-stu-id="8785c-122">The *pParticipant* or the *pITSubStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="8785c-123"><dt>**\_elementos TAPI E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="8785c-124">La subsecuencia no está lista.</span><span class="sxs-lookup"><span data-stu-id="8785c-124">The substream is not ready.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="8785c-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="8785c-126">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8785c-126">Insufficient memory exists to perform the operation.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="8785c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8785c-127">Requirements</span></span>



| <span data-ttu-id="8785c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8785c-128">Requirement</span></span> | <span data-ttu-id="8785c-129">Value</span><span class="sxs-lookup"><span data-stu-id="8785c-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8785c-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8785c-130">TAPI version</span></span><br/> | <span data-ttu-id="8785c-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8785c-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8785c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8785c-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8785c-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="8785c-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8785c-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8785c-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8785c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8785c-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8785c-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8785c-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8785c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8785c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8785c-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="8785c-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="8785c-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="8785c-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="8785c-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="8785c-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="8785c-142">**ITTerminal**</span><span class="sxs-lookup"><span data-stu-id="8785c-142">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

