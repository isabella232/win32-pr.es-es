---
description: Los controles de encuentro TAPI 3 permiten a los programadores crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferencias de telefonía IP de encuentro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276795"
---
# <a name="rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="a00af-103">Conferencias de telefonía IP de encuentro</span><span class="sxs-lookup"><span data-stu-id="a00af-103">Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="a00af-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a00af-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a00af-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a00af-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a00af-106">Los controles de encuentro TAPI 3 permiten a los programadores crear aplicaciones que pueden crear y detectar conferencias IP de multidifusión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a00af-106">The TAPI 3 Rendezvous controls enable a programmer to create applications that can create and discover multimedia multicast IP conferences.</span></span>

<span data-ttu-id="a00af-107">Los componentes clave de Rendezvous:</span><span class="sxs-lookup"><span data-stu-id="a00af-107">The key components of Rendezvous:</span></span>

<span data-ttu-id="a00af-108">[Los controles de directorio](directory-controls.md) son una abstracción de las listas de conferencias en un servidor ILS o Ntds.</span><span class="sxs-lookup"><span data-stu-id="a00af-108">[Directory Controls](directory-controls.md) are an abstraction of conference listings on an ILS or NTDS server.</span></span>

<span data-ttu-id="a00af-109">[Los controles de BLOB de conferencia](conference-blob-controls.md) representan información específica de la Conferencia, como la hora de inicio y de finalización.</span><span class="sxs-lookup"><span data-stu-id="a00af-109">[Conference Blob Controls](conference-blob-controls.md) represent conference-specific information such as start and stop time.</span></span> <span data-ttu-id="a00af-110">Se proporcionan interfaces especiales para los blobs de protocolo SDP.</span><span class="sxs-lookup"><span data-stu-id="a00af-110">Special interfaces are provided for SDP protocol blobs.</span></span> <span data-ttu-id="a00af-111">Para obtener información detallada, consulte RFC 2327 titulado "SDP: Protocolo de descripción de la sesión".</span><span class="sxs-lookup"><span data-stu-id="a00af-111">For detailed information, see RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="a00af-112">Se puede encontrar una copia actual de esta RFC mediante un motor de búsqueda de Internet.</span><span class="sxs-lookup"><span data-stu-id="a00af-112">A current copy of this RFC can be located using an Internet search engine.</span></span>

<span data-ttu-id="a00af-113">Las [interfaces com multidifusión](multicast-com-interfaces.md) son contenedores com para las funciones MADCAP, anteriormente conocido como MDHCP.</span><span class="sxs-lookup"><span data-stu-id="a00af-113">[Multicast COM Interfaces](multicast-com-interfaces.md) are COM wrappers for the MADCAP functions, formerly know as MDHCP.</span></span> <span data-ttu-id="a00af-114">Estas interfaces permiten a una aplicación obtener direcciones de multidifusión de un servidor de asignación de direcciones de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="a00af-114">These interfaces allow an application to get multicast addresses from a multicast address allocation server.</span></span>

<span data-ttu-id="a00af-115">En el material siguiente se proporciona información general y algunos ejemplos de uso de los controles Rendezvous para telefonía IP y conferencias.</span><span class="sxs-lookup"><span data-stu-id="a00af-115">The following material provides a general overview and some usage examples of the Rendezvous controls for IP telephony and conferencing.</span></span>

 

 



