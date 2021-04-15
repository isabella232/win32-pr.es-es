---
description: Para establecer una conexión entre un cliente y un servidor mediante el protocolo SMB de Microsoft, primero debe determinar el dialecto con el nivel más alto de funcionalidad que admiten tanto el cliente como el servidor.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialectos del protocolo SMB de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497302"
---
# <a name="microsoft-smb-protocol-dialects"></a><span data-ttu-id="3e28c-103">Dialectos del protocolo SMB de Microsoft</span><span class="sxs-lookup"><span data-stu-id="3e28c-103">Microsoft SMB Protocol Dialects</span></span>

<span data-ttu-id="3e28c-104">La lista de paquetes de mensajes del protocolo SMB de Microsoft ha crecido a lo largo de los años para adaptarse a la creciente funcionalidad del protocolo SMB de Microsoft y ahora tiene un número de cientos.</span><span class="sxs-lookup"><span data-stu-id="3e28c-104">The list of Microsoft SMB Protocol message packets has grown over the years to accommodate the increasing functionality of Microsoft SMB Protocol, and now numbers in the hundreds.</span></span> <span data-ttu-id="3e28c-105">Cada fase de su crecimiento se marca mediante un conjunto de paquetes estándar o dialecto.</span><span class="sxs-lookup"><span data-stu-id="3e28c-105">Each stage of its growth is marked by a standard packet set, or dialect.</span></span> <span data-ttu-id="3e28c-106">Cada dialecto se identifica mediante una cadena estándar como "PC NETWORK PROGRAM 1,0", "MICROSOFT NETWORKs 3,0", "DOS LANMAN 2,1" o "NT LM 0,12".</span><span class="sxs-lookup"><span data-stu-id="3e28c-106">Each dialect is identified by a standard string such as "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1", or "NT LM 0.12".</span></span> <span data-ttu-id="3e28c-107">La primera cadena identifica el primer dialecto de SMB y la última cadena identifica CIFS, el primer dialecto del protocolo SMB de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e28c-107">The first string identifies the first dialect of SMB, and the last string identifies CIFS, the first dialect of Microsoft SMB Protocol.</span></span>

<span data-ttu-id="3e28c-108">La mayoría de los clientes de Windows admiten al menos seis dialectos diferentes del protocolo SMB de Microsoft, por lo que uno de los primeros pasos para establecer una conexión entre un cliente y un servidor mediante el protocolo SMB de Microsoft es determinar el dialecto con el nivel máximo de funcionalidad que admiten tanto el cliente como el servidor.</span><span class="sxs-lookup"><span data-stu-id="3e28c-108">Most Windows clients support at least six different dialects of Microsoft SMB Protocol, so one of the first steps in establishing a connection between a client and a server using Microsoft SMB Protocol is to determine the dialect with the highest level of functionality that both the client and server support.</span></span> <span data-ttu-id="3e28c-109">Este proceso se conoce como "negociar el dialecto".</span><span class="sxs-lookup"><span data-stu-id="3e28c-109">This process is known as "negotiating the dialect."</span></span> <span data-ttu-id="3e28c-110">Las cadenas de dialecto mencionadas anteriormente se incluyen en los paquetes de solicitud y respuesta de negociación de dialecto para este fin.</span><span class="sxs-lookup"><span data-stu-id="3e28c-110">The dialect strings mentioned above are included in the dialect negotiation request and response packets for this purpose.</span></span>

 

 



