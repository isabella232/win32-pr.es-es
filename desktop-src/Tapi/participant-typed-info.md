---
description: 'Los miembros de la \_ enumeración información con tipo de participante \_ identifican el tipo de información de participante que recupera el método ITParticipant:: get \_ ParticipantTypedInfo. Esta enumeración la usan las aplicaciones que acceden a IPConf MSP.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Enumeración PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679488"
---
# <a name="participant_typed_info-enumeration"></a><span data-ttu-id="a9ede-104">\_Enumeración de información con tipo de participante \_</span><span class="sxs-lookup"><span data-stu-id="a9ede-104">PARTICIPANT\_TYPED\_INFO enumeration</span></span>

<span data-ttu-id="a9ede-105">\[**Participante \_ La \_ información con tipo** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a9ede-105">\[**PARTICIPANT\_TYPED\_INFO** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a9ede-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a9ede-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a9ede-107">Los miembros de la enumeración **\_ \_ información con tipo de participante** identifican el tipo de información de participante que recupera el método [**ITParticipant:: get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a9ede-107">The members of the **PARTICIPANT\_TYPED\_INFO** enum identify the type of participant information being retrieved by the [**ITParticipant::get\_ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) method.</span></span> <span data-ttu-id="a9ede-108">Esta enumeración la usan las aplicaciones que acceden a [IPCONF MSP](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="a9ede-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ede-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9ede-109">Syntax</span></span>


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a><span data-ttu-id="a9ede-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="a9ede-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a9ede-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**</span><span class="sxs-lookup"><span data-stu-id="a9ede-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI\_CANONICALNAME**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-112">Nombre canónico del participante, como someone@example.com .</span><span class="sxs-lookup"><span data-stu-id="a9ede-112">Canonical name of participant, such as someone@example.com.</span></span>

</dd> <dt>

<span data-ttu-id="a9ede-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**nombre de PTI \_**</span><span class="sxs-lookup"><span data-stu-id="a9ede-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI\_NAME**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-114">Nombre para mostrar del participante.</span><span class="sxs-lookup"><span data-stu-id="a9ede-114">Displayable name of participant.</span></span>

</dd> <dt>

<span data-ttu-id="a9ede-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EmailAddress**</span><span class="sxs-lookup"><span data-stu-id="a9ede-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI\_EMAILADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-116">Dirección de correo electrónico del participante.</span><span class="sxs-lookup"><span data-stu-id="a9ede-116">Participant's email address.</span></span>

</dd> <dt>

<span data-ttu-id="a9ede-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="a9ede-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI\_PHONENUMBER**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-118">Dirección de teléfono del participante.</span><span class="sxs-lookup"><span data-stu-id="a9ede-118">Participant's phone address.</span></span>

</dd> <dt>

<span data-ttu-id="a9ede-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**Ubicación de PTI \_**</span><span class="sxs-lookup"><span data-stu-id="a9ede-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI\_LOCATION**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-120">Dirección geográfica del participante.</span><span class="sxs-lookup"><span data-stu-id="a9ede-120">Participant's geographical address.</span></span>

</dd> <dt>

<span data-ttu-id="a9ede-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_herramienta PTI**</span><span class="sxs-lookup"><span data-stu-id="a9ede-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI\_TOOL**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-122">Aplicación del participante.</span><span class="sxs-lookup"><span data-stu-id="a9ede-122">Participant's application.</span></span>

</dd> <dt>

<span data-ttu-id="a9ede-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**Notas de PTI \_**</span><span class="sxs-lookup"><span data-stu-id="a9ede-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI\_NOTES**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-124">Notas sobre el participante.</span><span class="sxs-lookup"><span data-stu-id="a9ede-124">Notes concerning participant.</span></span>

</dd> <dt>

<span data-ttu-id="a9ede-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ privado**</span><span class="sxs-lookup"><span data-stu-id="a9ede-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="a9ede-126">Define una extensión experimental o de descripción de origen específica de la aplicación (SDES).</span><span class="sxs-lookup"><span data-stu-id="a9ede-126">Defines an experimental or application-specific Source Description (SDES) extension.</span></span> <span data-ttu-id="a9ede-127">Consulte RFC 1889 para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a9ede-127">See RFC 1889 for details.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9ede-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9ede-128">Requirements</span></span>



| <span data-ttu-id="a9ede-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ede-129">Requirement</span></span> | <span data-ttu-id="a9ede-130">Value</span><span class="sxs-lookup"><span data-stu-id="a9ede-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ede-131">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a9ede-131">TAPI version</span></span><br/> | <span data-ttu-id="a9ede-132">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a9ede-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a9ede-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9ede-133">Header</span></span><br/>       | <dl> <span data-ttu-id="a9ede-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ede-134"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ede-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9ede-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ede-136">**ITParticipant:: get \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="a9ede-136">**ITParticipant::get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[<span data-ttu-id="a9ede-137">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="a9ede-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="a9ede-138">Interfaces de IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="a9ede-138">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




