---
description: Los controles TAPI 3 Rendezvous proporcionan mecanismos para anunciar y detectar conferencias IP de multimedia multiparte. A continuación se describe un conjunto de componentes de modelo de objetos componentes (COM) e interfaces para implementar las conferencias.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Acerca de las conferencias de telefonía IP de Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566906"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="43804-104">Acerca de las conferencias de telefonía IP de Rendezvous</span><span class="sxs-lookup"><span data-stu-id="43804-104">About Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="43804-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="43804-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43804-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="43804-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="43804-107">Los controles TAPI 3 Rendezvous proporcionan mecanismos para anunciar y detectar conferencias IP de multimedia multiparte.</span><span class="sxs-lookup"><span data-stu-id="43804-107">The TAPI 3 Rendezvous controls provide mechanisms to advertise and discover multiparty multimedia IP conferences.</span></span> <span data-ttu-id="43804-108">A continuación se describe un conjunto de componentes de modelo de objetos componentes (COM) e interfaces para implementar las conferencias.</span><span class="sxs-lookup"><span data-stu-id="43804-108">The following describes a set of Component Object Model (COM) components and interfaces to implement conferencing.</span></span>

<span data-ttu-id="43804-109">COM es el modelo de codificación básica para TAPI 3 y está familiarizado con él en este documento.</span><span class="sxs-lookup"><span data-stu-id="43804-109">COM is the basic coding model for TAPI 3, and familiarity with it is assumed throughout this document.</span></span> <span data-ttu-id="43804-110">Para obtener información sobre COM, busque el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="43804-110">For information on COM, search the Platform Software Development Kit (SDK).</span></span>

## <a name="features"></a><span data-ttu-id="43804-111">Características</span><span class="sxs-lookup"><span data-stu-id="43804-111">Features</span></span>

-   <span data-ttu-id="43804-112">Proporciona la abstracción de un directorio de conferencias para manipular anuncios de conferencias multimedia</span><span class="sxs-lookup"><span data-stu-id="43804-112">Provides the abstraction of a conference directory for manipulating announcements of multimedia conferences</span></span>
-   <span data-ttu-id="43804-113">Proporciona seguridad a través de la autenticación, el cifrado y una capa de control de acceso (ACL) por anuncio.</span><span class="sxs-lookup"><span data-stu-id="43804-113">Provides security through authentication, encryption, and a per-announcement access control layer (ACL)</span></span>
-   <span data-ttu-id="43804-114">Proporciona un esquema común para un anuncio de conferencia, habilitando búsquedas por valores de atributo</span><span class="sxs-lookup"><span data-stu-id="43804-114">Provides a common schema for a conference announcement, enabling searches by attribute values</span></span>
-   <span data-ttu-id="43804-115">Permite extensiones a través de un atributo mantenido por el proveedor (BLOB de conferencia) en el esquema.</span><span class="sxs-lookup"><span data-stu-id="43804-115">Allows extensions through a provider-maintained attribute (conference blob) in the schema</span></span>
-   <span data-ttu-id="43804-116">Proporciona un contenedor COM para la API de asignación de direcciones de multidifusión (MADCAP)</span><span class="sxs-lookup"><span data-stu-id="43804-116">Provides a COM wrapper for the multicast address allocation (MADCAP) API</span></span>

## <a name="architecture"></a><span data-ttu-id="43804-117">Architecture</span><span class="sxs-lookup"><span data-stu-id="43804-117">Architecture</span></span>

<span data-ttu-id="43804-118">En las descripciones y diagramas siguientes se muestran los aspectos clave de la arquitectura del sistema.</span><span class="sxs-lookup"><span data-stu-id="43804-118">The following descriptions and diagram illustrate key aspects of the system architecture.</span></span>

-   <span data-ttu-id="43804-119">El cliente puede manipular las conferencias almacenadas en un directorio dinámico ILS o en un servidor NTDS mediante controles Rendezvous.</span><span class="sxs-lookup"><span data-stu-id="43804-119">The client can manipulate conferences stored on an ILS dynamic directory or NTDS server using Rendezvous controls.</span></span> <span data-ttu-id="43804-120">El Protocolo ligero de acceso a directorios (LDAP) se usa para comunicarse con un servidor ILS.</span><span class="sxs-lookup"><span data-stu-id="43804-120">The Lightweight Directory Access Protocol (LDAP) is used to communicate with an ILS server.</span></span>
-   <span data-ttu-id="43804-121">Los controles Rendezvous proporcionan interfaces COM duales para el scripting y la programación.</span><span class="sxs-lookup"><span data-stu-id="43804-121">The Rendezvous controls provide dual COM interfaces for scripting and programming.</span></span>
-   <span data-ttu-id="43804-122">Un servidor de protocolo de anuncio de sesión (SAP) con acceso directo a Internet escucha los anuncios de conferencias en Internet y rellena los servidores ILS dinámicos con la información de la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="43804-122">A Session Announcement Protocol (SAP) server with direct access to the Internet listens to conference announcements on the Internet and populates ILS dynamic servers with the conference information.</span></span> <span data-ttu-id="43804-123">De forma similar, también anuncia las conferencias creadas localmente cuyo ámbito incluye Internet.</span><span class="sxs-lookup"><span data-stu-id="43804-123">Similarly, it also announces the locally created conferences whose scope includes the Internet.</span></span> <span data-ttu-id="43804-124">(El servidor SAP no está planeado para Microsoft Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="43804-124">(The SAP server is not planned for Microsoft Windows 2000.)</span></span>

![arquitectura del sistema Rendezvous](images/rend1.png)

 

 



