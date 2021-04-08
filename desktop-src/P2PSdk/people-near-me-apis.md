---
description: API de equipos a mi alrededor
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: API de equipos a mi alrededor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001996"
---
# <a name="people-near-me-apis"></a><span data-ttu-id="7466f-103">API de equipos a mi alrededor</span><span class="sxs-lookup"><span data-stu-id="7466f-103">People Near Me APIs</span></span>

<span data-ttu-id="7466f-104">Cualquier aplicación que pueda usar [People Near me](about-people-near-me.md) (PNM) puede utilizar las siguientes API de Win32:</span><span class="sxs-lookup"><span data-stu-id="7466f-104">Any applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following Win32 APIs:</span></span>

### <a name="contacts-api"></a><span data-ttu-id="7466f-105">API de contactos</span><span class="sxs-lookup"><span data-stu-id="7466f-105">Contacts API</span></span>

<span data-ttu-id="7466f-106">La API de contactos se usa para obtener acceso a la información de contacto del usuario que ha iniciado sesión, recuperar información acerca de los contactos previamente almacenados o almacenar la información de contacto y el certificado digital de un nuevo contacto.</span><span class="sxs-lookup"><span data-stu-id="7466f-106">The Contacts API is used to access the contact information for the logged on user, retrieve information about previously stored contacts, or store the contact information and digital certificate of a new contact.</span></span>

### <a name="people-near-me-api"></a><span data-ttu-id="7466f-107">API de equipos a mi alrededor</span><span class="sxs-lookup"><span data-stu-id="7466f-107">People Near Me API</span></span>

<span data-ttu-id="7466f-108">La API PNM se usa para buscar usuarios cercanos, sus intereses anunciados, cualquier objeto arbitrario que decida publicar y aplicaciones anunciadas.</span><span class="sxs-lookup"><span data-stu-id="7466f-108">The PNM API is used to find users nearby, their advertised interests, any arbitrary objects they choose to publish, and advertised applications.</span></span>

### <a name="publication-api"></a><span data-ttu-id="7466f-109">API de publicación</span><span class="sxs-lookup"><span data-stu-id="7466f-109">Publication API</span></span>

<span data-ttu-id="7466f-110">La API de publicación se usa para interactuar con los contactos remotos.</span><span class="sxs-lookup"><span data-stu-id="7466f-110">The Publication API is used to interact with remote contacts.</span></span> <span data-ttu-id="7466f-111">El módulo PNM también usa la capa de [señal del mismo nivel](windows-peer-components-for-people-near-me.md) usada por el administrador de publicación para establecer conexiones.</span><span class="sxs-lookup"><span data-stu-id="7466f-111">The [Peer Signaling](windows-peer-components-for-people-near-me.md) layer used by the Publication Manager is also used by the PNM module for establishing connections.</span></span>

### <a name="invitation-api"></a><span data-ttu-id="7466f-112">API de invitación</span><span class="sxs-lookup"><span data-stu-id="7466f-112">Invitation API</span></span>

<span data-ttu-id="7466f-113">Una aplicación de colaboración usa la API de invitación para invitar a un par específico a una actividad de colaboración.</span><span class="sxs-lookup"><span data-stu-id="7466f-113">The Invitation API is used by a collaboration application to invite specific peer(s) into a collaboration activity.</span></span>

### <a name="application-registration-api"></a><span data-ttu-id="7466f-114">API de registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7466f-114">Application Registration API</span></span>

<span data-ttu-id="7466f-115">El instalador de una aplicación de colaboración usa la API de registro de aplicaciones para registrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7466f-115">The Application Registration API is used by the installer of a collaboration application to register the application.</span></span> <span data-ttu-id="7466f-116">Una aplicación compatible con PNM le pedirá al usuario durante el proceso de instalación para determinar si la aplicación debe estar disponible para los usuarios en la subred.</span><span class="sxs-lookup"><span data-stu-id="7466f-116">A PNM-capable application will prompt the user during the installation process to determine whether the application should be made available to users on the subnet.</span></span>

 

 



