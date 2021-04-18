---
description: La \_ enumeración del juego de caracteres de blob \_ indica el juego de caracteres utilizado por el BLOB de la Conferencia actual.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Enumeración BLOB_CHARACTER_SET (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680404"
---
# <a name="blob_character_set-enumeration"></a><span data-ttu-id="cf058-103">\_Enumeración de juegos de caracteres de blob \_</span><span class="sxs-lookup"><span data-stu-id="cf058-103">BLOB\_CHARACTER\_SET enumeration</span></span>

<span data-ttu-id="cf058-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cf058-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf058-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="cf058-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cf058-106">La enumeración del **\_ \_ juego de caracteres de BLOB** indica el juego de caracteres utilizado por el BLOB de la Conferencia actual.</span><span class="sxs-lookup"><span data-stu-id="cf058-106">The **BLOB\_CHARACTER\_SET** enum indicates the character set used by the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf058-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf058-107">Syntax</span></span>


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a><span data-ttu-id="cf058-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="cf058-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf058-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**ASCII de BCS \_**</span><span class="sxs-lookup"><span data-stu-id="cf058-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS\_ASCII**</span></span>
</dt> <dd>

<span data-ttu-id="cf058-110">Formato ASCII estándar.</span><span class="sxs-lookup"><span data-stu-id="cf058-110">Standard ASCII format.</span></span>

</dd> <dt>

<span data-ttu-id="cf058-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**UTF7 de BCS \_**</span><span class="sxs-lookup"><span data-stu-id="cf058-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS\_UTF7**</span></span>
</dt> <dd>

<span data-ttu-id="cf058-112">Formato de transformación de siete bits de Unicode.</span><span class="sxs-lookup"><span data-stu-id="cf058-112">Seven-bit transformation format of Unicode.</span></span> <span data-ttu-id="cf058-113">Para obtener más información sobre este formato, realice una búsqueda en Internet de RFC 1642.</span><span class="sxs-lookup"><span data-stu-id="cf058-113">For details on this format, conduct an Internet search for RFC 1642.</span></span>

</dd> <dt>

<span data-ttu-id="cf058-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**UTF8 de BCS \_**</span><span class="sxs-lookup"><span data-stu-id="cf058-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS\_UTF8**</span></span>
</dt> <dd>

<span data-ttu-id="cf058-115">Formato de transformación UCS 8.</span><span class="sxs-lookup"><span data-stu-id="cf058-115">UCS Transformation Format 8.</span></span> <span data-ttu-id="cf058-116">Para obtener más información sobre este formato, realice una búsqueda en Internet de ISO (el Organización internacional de normalización) e IEC (el Comisión electrotécnica internacional (CEI)) documento ISO/IEC JTC1/SC2/WG2 N 1036, con fecha del 1 de agosto de 1994, por el editor de proyectos de WG2.</span><span class="sxs-lookup"><span data-stu-id="cf058-116">For details on this format, conduct an Internet search for ISO (the International Organization for Standardization) and IEC (the International Electrotechnical Commission) document ISO/IEC JTC1/SC2/WG2 N 1036, dated August 1, 1994, by WG2 Project Editor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf058-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf058-117">Requirements</span></span>



| <span data-ttu-id="cf058-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf058-118">Requirement</span></span> | <span data-ttu-id="cf058-119">Value</span><span class="sxs-lookup"><span data-stu-id="cf058-119">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf058-120">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="cf058-120">TAPI version</span></span><br/> | <span data-ttu-id="cf058-121">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cf058-121">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="cf058-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf058-122">Header</span></span><br/>       | <dl> <span data-ttu-id="cf058-123"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf058-123"><dt>Sdpblb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf058-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf058-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf058-125">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="cf058-125">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[<span data-ttu-id="cf058-126">**obtener \_ characterSet**</span><span class="sxs-lookup"><span data-stu-id="cf058-126">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)
</dt> <dt>

[<span data-ttu-id="cf058-127">**Smss**</span><span class="sxs-lookup"><span data-stu-id="cf058-127">**Init**</span></span>](itconferenceblob-init.md)
</dt> <dt>

[<span data-ttu-id="cf058-128">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="cf058-128">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




