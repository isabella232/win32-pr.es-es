---
description: En el diagrama siguiente se muestran los objetos principales implicados en los controles de directorio TAPI 3 Rendezvous. Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Controles de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677384"
---
# <a name="directory-controls"></a><span data-ttu-id="0b58d-104">Controles de directorio</span><span class="sxs-lookup"><span data-stu-id="0b58d-104">Directory Controls</span></span>

<span data-ttu-id="0b58d-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b58d-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0b58d-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0b58d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0b58d-107">En el diagrama siguiente se muestran los objetos principales implicados en los controles de directorio TAPI 3 Rendezvous.</span><span class="sxs-lookup"><span data-stu-id="0b58d-107">The following diagram illustrates the main objects involved in TAPI 3 Rendezvous directory controls.</span></span> <span data-ttu-id="0b58d-108">Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.</span><span class="sxs-lookup"><span data-stu-id="0b58d-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![objetos e interfaces del control de directorio Rendezvous](images/renddir.png)

<span data-ttu-id="0b58d-110">La interfaz principal de control de directorios es [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), que se debe crear mediante una llamada a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="0b58d-110">The main directory control interface is [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), which must be created by calling **CoCreateInstance**.</span></span> <span data-ttu-id="0b58d-111">El objeto Rendezvous expone métodos para obtener listas de directorios disponibles y para crear nuevos directorios o objetos de directorio.</span><span class="sxs-lookup"><span data-stu-id="0b58d-111">The Rendezvous object exposes methods to get lists of available directories and to create new directories or directory objects.</span></span>

<span data-ttu-id="0b58d-112">Un directorio reside en un servidor y es una lista de objetos de directorio junto con información descriptiva.</span><span class="sxs-lookup"><span data-stu-id="0b58d-112">A directory resides on a server and is a list of directory objects along with descriptive information.</span></span> <span data-ttu-id="0b58d-113">Los métodos asociados a [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) pueden obtener información asociada al directorio como un todo, por ejemplo, si se trata de un directorio ILS.</span><span class="sxs-lookup"><span data-stu-id="0b58d-113">Methods associated with [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) can get information associated with the directory as a whole, such as whether it is an ILS directory.</span></span>

<span data-ttu-id="0b58d-114">Un objeto de directorio puede representar una conferencia o un usuario.</span><span class="sxs-lookup"><span data-stu-id="0b58d-114">A directory object can represent a conference or a user.</span></span> <span data-ttu-id="0b58d-115">La interfaz [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) proporciona métodos que pueden recuperar o modificar información genérica de un objeto de directorio, como la dirección de marcado.</span><span class="sxs-lookup"><span data-stu-id="0b58d-115">The [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) interface supplies methods that can retrieve or modify information generic to a directory object, such as the dialable address.</span></span>

<span data-ttu-id="0b58d-116">La información de conferencia y usuario, como la dirección URL de una conferencia o el teléfono IP principal de un usuario, se manipula mediante métodos proporcionados en las interfaces [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) y [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .</span><span class="sxs-lookup"><span data-stu-id="0b58d-116">Conference and user information, such as the URL of a conference or the primary IP phone of a user, is manipulated by methods provided in the [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) and [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) interfaces.</span></span>

 

 



