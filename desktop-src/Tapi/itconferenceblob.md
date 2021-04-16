---
description: Manipula una descripción de la Conferencia textual.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interfaz ITConferenceBlob (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690436"
---
# <a name="itconferenceblob-interface"></a><span data-ttu-id="581e0-103">Interfaz ITConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="581e0-103">ITConferenceBlob interface</span></span>

<span data-ttu-id="581e0-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="581e0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="581e0-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="581e0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="581e0-106">La interfaz **ITConferenceBlob** manipula una descripción de la Conferencia textual.</span><span class="sxs-lookup"><span data-stu-id="581e0-106">The **ITConferenceBlob** interface manipulates a textual conference description.</span></span> <span data-ttu-id="581e0-107">La interfaz está pensada para ser independiente del formato y la sintaxis de la descripción de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="581e0-107">The interface is intended to be independent of the format and syntax of the conference description.</span></span> <span data-ttu-id="581e0-108">Para manipular aspectos específicos de la descripción de la Conferencia, la aplicación debe consultar otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="581e0-108">To manipulate specific aspects of the conference description, the application must query for another interface.</span></span> <span data-ttu-id="581e0-109">Actualmente, solo se admiten las descripciones de la Conferencia SDP; la aplicación debe usar **QueryInterface** para [**ITSdp**](itsdp.md) para tener acceso a los distintos campos de la descripción de la Conferencia SDP.</span><span class="sxs-lookup"><span data-stu-id="581e0-109">Currently, only SDP conference descriptions are supported; the application must use **QueryInterface** for [**ITSdp**](itsdp.md) to access the various fields of the SDP conference description.</span></span> <span data-ttu-id="581e0-110">La interfaz **ITConferenceBlob** se crea llamando a **QueryInterface** en [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="581e0-110">The **ITConferenceBlob** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="581e0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="581e0-111">Members</span></span>

<span data-ttu-id="581e0-112">La interfaz **ITConferenceBlob** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="581e0-112">The **ITConferenceBlob** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="581e0-113">**ITConferenceBlob** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="581e0-113">**ITConferenceBlob** also has these types of members:</span></span>

-   [<span data-ttu-id="581e0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="581e0-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="581e0-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="581e0-115">Methods</span></span>

<span data-ttu-id="581e0-116">La interfaz **ITConferenceBlob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="581e0-116">The **ITConferenceBlob** interface has these methods.</span></span>



| <span data-ttu-id="581e0-117">Método</span><span class="sxs-lookup"><span data-stu-id="581e0-117">Method</span></span>                                                             | <span data-ttu-id="581e0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="581e0-118">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="581e0-119">**obtener \_ characterSet**</span><span class="sxs-lookup"><span data-stu-id="581e0-119">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)     | <span data-ttu-id="581e0-120">Obtiene el indicador del [**\_ \_ juego de caracteres de BLOB**](blob-character-set.md) de si los caracteres de BLOB están en ASCII, Unicode, etc.</span><span class="sxs-lookup"><span data-stu-id="581e0-120">Gets the [**BLOB\_CHARACTER\_SET**](blob-character-set.md) indicator of whether blob characters are in ASCII, Unicode, and so on.</span></span><br/> |
| [<span data-ttu-id="581e0-121">**obtener \_ ConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="581e0-121">**get\_ConferenceBlob**</span></span>](itconferenceblob-get-conferenceblob.md) | <span data-ttu-id="581e0-122">Obtiene un puntero al BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="581e0-122">Gets a pointer to the conference blob.</span></span><br/>                                                                                             |
| [<span data-ttu-id="581e0-123">**Smss**</span><span class="sxs-lookup"><span data-stu-id="581e0-123">**Init**</span></span>](itconferenceblob-init.md)                              | <span data-ttu-id="581e0-124">Inicializa el BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="581e0-124">Initializes the conference blob.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="581e0-125">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="581e0-125">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)    | <span data-ttu-id="581e0-126">Confirma los cambios en el BLOB de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="581e0-126">Commits changes to the conference blob.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="581e0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="581e0-127">Requirements</span></span>



| <span data-ttu-id="581e0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="581e0-128">Requirement</span></span> | <span data-ttu-id="581e0-129">Value</span><span class="sxs-lookup"><span data-stu-id="581e0-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="581e0-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="581e0-130">TAPI version</span></span><br/> | <span data-ttu-id="581e0-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="581e0-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="581e0-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="581e0-132">Header</span></span><br/>       | <dl> <span data-ttu-id="581e0-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="581e0-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="581e0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="581e0-134">Library</span></span><br/>      | <dl> <span data-ttu-id="581e0-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="581e0-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="581e0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="581e0-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="581e0-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="581e0-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

