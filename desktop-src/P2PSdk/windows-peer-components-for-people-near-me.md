---
description: Componentes del mismo nivel de Windows para People Near me
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Componentes del mismo nivel de Windows para People Near me
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001988"
---
# <a name="windows-peer-components-for-people-near-me"></a><span data-ttu-id="a9d87-103">Componentes del mismo nivel de Windows para People Near me</span><span class="sxs-lookup"><span data-stu-id="a9d87-103">Windows Peer Components for People Near Me</span></span>

<span data-ttu-id="a9d87-104">Dentro del archivo ejecutable principal de redes del mismo nivel de Windows (P2phost.exe), la [arquitectura People Near me](people-near-me-architecture.md) usa los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="a9d87-104">Within the main Windows Peer Networking executable (P2phost.exe), the [People Near Me Architecture](people-near-me-architecture.md) uses the following components:</span></span>

### <a name="people-near-me"></a><span data-ttu-id="a9d87-105">People Near Me (Gente que esté cerca)</span><span class="sxs-lookup"><span data-stu-id="a9d87-105">People Near Me</span></span>

<span data-ttu-id="a9d87-106">El componente equipos a mi alrededor (PNM) inicia la detección mediante el descubrimiento de servicios web en la subred local para los nombres de usuario de equipos compatibles con PNM.</span><span class="sxs-lookup"><span data-stu-id="a9d87-106">The People Near Me (PNM) component initiates discovery using Web Services Discovery on the local subnet for the user names of PNM-capable computers.</span></span>

### <a name="people-near-me-publisher"></a><span data-ttu-id="a9d87-107">Publicador de equipos a mi alrededor</span><span class="sxs-lookup"><span data-stu-id="a9d87-107">People Near Me Publisher</span></span>

<span data-ttu-id="a9d87-108">El componente de publicador de equipos a mi alrededor publica los alias de los usuarios que han iniciado sesión para indicar la disponibilidad de otros equipos que usan PNM en la subred local.</span><span class="sxs-lookup"><span data-stu-id="a9d87-108">The People Near Me Publisher component publishes the nicknames of logged-on users to indicate availability to other computers using PNM on the local subnet.</span></span> <span data-ttu-id="a9d87-109">El usuario que ha iniciado sesión debe elegir publicar su alias antes de que se anuncie.</span><span class="sxs-lookup"><span data-stu-id="a9d87-109">The logged-on user must elect to publish their nickname before it is advertised.</span></span> <span data-ttu-id="a9d87-110">El alias se publica en la subred mediante la detección de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="a9d87-110">The nickname is published on the subnet using Web Services Discovery.</span></span> <span data-ttu-id="a9d87-111">Además, también se pueden publicar objetos y aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a9d87-111">Additionally, objects and applications can also be published.</span></span> <span data-ttu-id="a9d87-112">Sin embargo, el usuario debe especificar la publicación de objetos y aplicaciones para los ámbitos "equipos a **mi alrededor**" o "**todos**".</span><span class="sxs-lookup"><span data-stu-id="a9d87-112">However, the user must specify object and application publication for the '**People Near Me**' or '**All**' scopes.</span></span>

### <a name="people-near-me-enumerator"></a><span data-ttu-id="a9d87-113">Enumerador de equipos a mi alrededor</span><span class="sxs-lookup"><span data-stu-id="a9d87-113">People Near Me Enumerator</span></span>

<span data-ttu-id="a9d87-114">El componente de enumerador People Near me enumera la lista de usuarios de la subred local.</span><span class="sxs-lookup"><span data-stu-id="a9d87-114">The People Near Me Enumerator component enumerates the list of users on the local subnet.</span></span> <span data-ttu-id="a9d87-115">Mediante esta lista, la detección de servicios Web envía una consulta de multidifusión y recibe las respuestas.</span><span class="sxs-lookup"><span data-stu-id="a9d87-115">Using this list, Web Services Discovery sends a multicast query and receives the responses.</span></span> <span data-ttu-id="a9d87-116">Una vez obtenida la lista de sobrenombres, una aplicación puede usar la API para recuperar más datos publicados por el usuario (cifrado mediante [Schannel](windows-vista-components-for-people-near-me.md)), como la lista de aplicaciones registradas y los objetos que se van a publicar.</span><span class="sxs-lookup"><span data-stu-id="a9d87-116">After the list of nicknames are obtained, an application can use the API to retrieve more data being published by the user (which is encrypted using [SChannel](windows-vista-components-for-people-near-me.md)), such as the list of applications registered and any objects being published.</span></span>

<span data-ttu-id="a9d87-117">El proceso de búsqueda y enumeración no se lleva a cabo automáticamente, pero debe iniciarse explícitamente por un usuario o una aplicación mediante el inicio de sesión en PNM.</span><span class="sxs-lookup"><span data-stu-id="a9d87-117">The search and enumeration process does not happen automatically, but must be explicitly initiated by a user or an application by signing-in to PNM.</span></span> <span data-ttu-id="a9d87-118">Los resultados de la búsqueda son la lista de alias de otros usuarios de la misma subred que están anunciando sus sobrenombres mediante la API de PNM.</span><span class="sxs-lookup"><span data-stu-id="a9d87-118">The search results are the list of nicknames of other users on the same subnet that are advertising their nicknames using the PNM API.</span></span>

### <a name="publication-manager"></a><span data-ttu-id="a9d87-119">Administrador de publicaciones</span><span class="sxs-lookup"><span data-stu-id="a9d87-119">Publication Manager</span></span>

<span data-ttu-id="a9d87-120">El componente del administrador de publicaciones es responsable de publicar las actualizaciones de presencia, aplicación o objeto en contactos o equipos a mi alrededor que estén suscritos o sondeen los datos.</span><span class="sxs-lookup"><span data-stu-id="a9d87-120">The Publication Manager component is responsible for publishing presence, application, or object updates to contacts or people near me that are subscribed or poll for data.</span></span>

### <a name="peer-signaling"></a><span data-ttu-id="a9d87-121">Señalización del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="a9d87-121">Peer Signaling</span></span>

<span data-ttu-id="a9d87-122">El componente de señalización del mismo nivel controla la creación de conexiones entre pares para intercambiar datos.</span><span class="sxs-lookup"><span data-stu-id="a9d87-122">The Peer Signaling component handles the creation of connections between peers to exchange data.</span></span> <span data-ttu-id="a9d87-123">En el caso de equipos a mi alrededor, la señalización del mismo nivel se usa cuando un usuario o una aplicación envía la consulta de unidifusión a un equipo específico para su clave pública, aplicaciones y objetos.</span><span class="sxs-lookup"><span data-stu-id="a9d87-123">For People Near Me, Peer Signaling is used when a user or application sends the unicast query to a specific computer for its public key, applications, and objects.</span></span>

### <a name="receive-invitation-handlerux"></a><span data-ttu-id="a9d87-124">Recibir identificador de invitación/UX</span><span class="sxs-lookup"><span data-stu-id="a9d87-124">Receive Invitation Handler/UX</span></span>

<span data-ttu-id="a9d87-125">El componente de la experiencia de usuario/controlador de invitación de recepción recibe una invitación entrante de otra persona, pide al usuario que determine si desea iniciar la aplicación asociada a la invitación y, a continuación, inicia la aplicación en función del usuario que acepta la invitación.</span><span class="sxs-lookup"><span data-stu-id="a9d87-125">The Receive Invitation Handler/UX component receives an incoming invitation from another person, prompts the user to determine whether they want to launch the application associated with the invitation, and then launches the application based on the user accepting the invitation.</span></span> <span data-ttu-id="a9d87-126">Una invitación es un mensaje de otra persona para iniciar la actividad de colaboración con una aplicación específica instalada en los equipos de los usuarios y anunciada por el usuario al que se va a invitar.</span><span class="sxs-lookup"><span data-stu-id="a9d87-126">An invitation is a message from another person to initiate collaboration activity using a specific application that is installed on both user's computers and is advertised by the user being invited.</span></span>

### <a name="peer-security"></a><span data-ttu-id="a9d87-127">Seguridad del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="a9d87-127">Peer Security</span></span>

<span data-ttu-id="a9d87-128">Cuando se envían la presencia, la aplicación y el objeto, la información se cifra mediante un canal SSL ([Schannel](windows-vista-components-for-people-near-me.md)).</span><span class="sxs-lookup"><span data-stu-id="a9d87-128">When presence, application, and object are sent, the information is encrypted using an SSL channel ([Schannel](windows-vista-components-for-people-near-me.md)).</span></span> <span data-ttu-id="a9d87-129">El equipo iniciador utiliza la clave pública del equipo invitado para negociar una clave secreta que se utiliza para cifrar los datos siguientes enviados entre los dos equipos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="a9d87-129">The initiating computer uses the public key of the invited computer to negotiate a secret key that is used for encrypting the subsequent data sent between the two peers.</span></span>

 

 



