---
description: TAPI asigna identificadores de sesión únicos para cada sesión y aplicación.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificador de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424071"
---
# <a name="session-identifier"></a><span data-ttu-id="3eae6-103">Identificador de sesión</span><span class="sxs-lookup"><span data-stu-id="3eae6-103">Session Identifier</span></span>

<span data-ttu-id="3eae6-104">TAPI asigna identificadores de sesión únicos para cada sesión y aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eae6-104">TAPI assigns session identifiers that are unique for each session and application.</span></span> <span data-ttu-id="3eae6-105">Una aplicación utiliza un identificador de sesión para comunicarse con TAPI en relación con una sesión específica.</span><span class="sxs-lookup"><span data-stu-id="3eae6-105">An application uses a session identifier to communicate with TAPI concerning a specific session.</span></span> <span data-ttu-id="3eae6-106">Normalmente, una aplicación obtiene un identificador mediante la creación de una nueva sesión de comunicaciones o cuando TAPI ofrece una sesión.</span><span class="sxs-lookup"><span data-stu-id="3eae6-106">An application typically obtains an identifier either by creating a new communications session or when TAPI offers a session.</span></span>

<span data-ttu-id="3eae6-107">No se puede usar un identificador de sesión para pasar información a otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="3eae6-107">A session identifier cannot be used to pass information to another application.</span></span> <span data-ttu-id="3eae6-108">Para este propósito, use el [identificador de llamada](call-id-ovr.md), que puede ser asignado por un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="3eae6-108">For this purpose, use the [Call ID](call-id-ovr.md), which may be assigned by a service provider.</span></span>

<span data-ttu-id="3eae6-109">Vea [iniciar una sesión](initiate-a-session-ovr.md) para obtener información sobre las operaciones que crean sesiones y devuelven un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="3eae6-109">See [Initiate a session](initiate-a-session-ovr.md) for information on operations that create sessions and return a session identifier.</span></span> <span data-ttu-id="3eae6-110">Vea [responder a una sesión iniciada en otro lugar](respond-to-session-initiated-elsewhere-ovr.md) para las operaciones que adquieren identificadores de sesión de TAPI.</span><span class="sxs-lookup"><span data-stu-id="3eae6-110">See [Respond to session initiated elsewhere](respond-to-session-initiated-elsewhere-ovr.md) for operations that acquire session identifiers from TAPI.</span></span> <span data-ttu-id="3eae6-111">Vea [finalizar una sesión](terminate-a-session-ovr.md) para obtener información sobre la liberación de recursos de sesión.</span><span class="sxs-lookup"><span data-stu-id="3eae6-111">See [Terminate a Session](terminate-a-session-ovr.md) for information on releasing session resources.</span></span>

<span data-ttu-id="3eae6-112">Todos los proveedores de servicios deben admitir algún tipo de identificación de sesión.</span><span class="sxs-lookup"><span data-stu-id="3eae6-112">All service providers must support some form of session identification.</span></span>

<span data-ttu-id="3eae6-113">**TAPI 2. x:** El identificador principal de una sesión de comunicaciones es el identificador de llamada.</span><span class="sxs-lookup"><span data-stu-id="3eae6-113">**TAPI 2.x:** The primary identifier of a communications session is the call handle.</span></span>

<span data-ttu-id="3eae6-114">**TAPI 3. x:** Una sesión se representa mediante un [objeto de llamada](call-object.md) y el identificador principal es un puntero a la interfaz [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="3eae6-114">**TAPI 3.x:** A session is represented by a [Call Object](call-object.md) and the primary identifier is a pointer to the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span>

 

 



