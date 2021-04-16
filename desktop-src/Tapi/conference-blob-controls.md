---
description: En el diagrama siguiente se muestran los objetos principales implicados en los controles de BLOB de la Conferencia TAPI 3. Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Controles de BLOB de conferencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542990"
---
# <a name="conference-blob-controls"></a><span data-ttu-id="b347f-104">Controles de BLOB de conferencia</span><span class="sxs-lookup"><span data-stu-id="b347f-104">Conference Blob Controls</span></span>

<span data-ttu-id="b347f-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b347f-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b347f-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b347f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b347f-107">En el diagrama siguiente se muestran los objetos principales implicados en los controles de BLOB de la Conferencia TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="b347f-107">The following diagram illustrates the main objects involved in TAPI 3 conference blob controls.</span></span> <span data-ttu-id="b347f-108">Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.</span><span class="sxs-lookup"><span data-stu-id="b347f-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![interfaces y controles de blobs en conferencias](images/rendblob.png)

<span data-ttu-id="b347f-110">El BLOB de la Conferencia contiene información específica del proveedor en un objeto de conferencia.</span><span class="sxs-lookup"><span data-stu-id="b347f-110">The conference blob contains provider-specific information on a conference object.</span></span> <span data-ttu-id="b347f-111">Un puntero al BLOB de la interfaz [**ITConferenceBlob**](itconferenceblob.md) se obtiene mediante QueryInterface en [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span><span class="sxs-lookup"><span data-stu-id="b347f-111">A pointer to the [**ITConferenceBlob**](itconferenceblob.md) interface blob is obtained by doing a QueryInterface on [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span></span> <span data-ttu-id="b347f-112">La interfaz **ITConferenceBlob** proporciona métodos para la manipulación básica de un BLOB de conferencia genérico.</span><span class="sxs-lookup"><span data-stu-id="b347f-112">The **ITConferenceBlob** interface provides methods for basic manipulation of a generic conference blob.</span></span> <span data-ttu-id="b347f-113">Una aplicación que usa blobs de conferencias no SDP debe implementar sus propios métodos para la manipulación detallada.</span><span class="sxs-lookup"><span data-stu-id="b347f-113">An application using non-SDP conference blobs must implement its own methods for detail manipulation.</span></span>

<span data-ttu-id="b347f-114">Rendezvous proporciona la interfaz [**ITSdp**](itsdp.md) para manipular los blobs de la Conferencia SDP.</span><span class="sxs-lookup"><span data-stu-id="b347f-114">Rendezvous provides the [**ITSdp**](itsdp.md) interface for manipulating SDP conference blobs.</span></span> <span data-ttu-id="b347f-115">SDP es un protocolo para describir las sesiones multimedia y su información de programación relacionada.</span><span class="sxs-lookup"><span data-stu-id="b347f-115">The SDP is a protocol for describing multimedia sessions and their related scheduling information.</span></span> <span data-ttu-id="b347f-116">Para obtener información adicional sobre el protocolo SDP, busque el RFC 2327 de Internet Engineering Task Force (IETF) titulado "SDP: Protocolo de descripción de la sesión".</span><span class="sxs-lookup"><span data-stu-id="b347f-116">For additional information on the SDP protocol, locate Internet Engineering Task Force (IETF) RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="b347f-117">Si la interfaz **ITSDP** existe para un BLOB de conferencia determinado, puede obtener un puntero a ella mediante **QueryInterface** en [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="b347f-117">If the **ITSDP** interface exists for a given conference blob, you can obtain a pointer to it by doing a **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

<span data-ttu-id="b347f-118">En el caso de los blobs de la Conferencia SDP, las interfaces [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)y [**ITMedia**](itmedia.md) permiten el control detallado del tiempo de conferencia SDP y de las características multimedia.</span><span class="sxs-lookup"><span data-stu-id="b347f-118">For SDP conference blobs, the [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md), and [**ITMedia**](itmedia.md) interfaces allow detailed control of SDP conference time and media characteristics.</span></span>

 

 



