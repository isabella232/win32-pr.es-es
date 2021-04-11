---
description: Tiendas de equipos a mi alrededor
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Tiendas de equipos a mi alrededor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911313"
---
# <a name="people-near-me-stores"></a><span data-ttu-id="6aeb8-103">Tiendas de equipos a mi alrededor</span><span class="sxs-lookup"><span data-stu-id="6aeb8-103">People Near Me Stores</span></span>

<span data-ttu-id="6aeb8-104">Las aplicaciones capaces de usar equipos a [mi alrededor](about-people-near-me.md) (PNM) pueden utilizar los siguientes almacenes de datos:</span><span class="sxs-lookup"><span data-stu-id="6aeb8-104">Applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following data stores:</span></span>

### <a name="windows-address-book"></a><span data-ttu-id="6aeb8-105">Libreta de direcciones de Windows</span><span class="sxs-lookup"><span data-stu-id="6aeb8-105">Windows Address Book</span></span>

<span data-ttu-id="6aeb8-106">La libreta de direcciones de Windows almacena información sobre los contactos y sus certificados digitales.</span><span class="sxs-lookup"><span data-stu-id="6aeb8-106">The Windows Address Book stores information on contacts and their digital certificates.</span></span> <span data-ttu-id="6aeb8-107">El contacto "**me**", que representa el usuario que ha iniciado la sesión, también se almacena en la libreta de direcciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="6aeb8-107">The '**Me**' contact, representing the currently logged in user, is also stored in the Windows Address Book.</span></span>

### <a name="certificate-store"></a><span data-ttu-id="6aeb8-108">Almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="6aeb8-108">Certificate Store</span></span>

<span data-ttu-id="6aeb8-109">El almacén de certificados contiene el certificado autofirmado para el contacto "**me**".</span><span class="sxs-lookup"><span data-stu-id="6aeb8-109">The Certificate Store contains the self-signed certificate for the '**Me**' contact.</span></span>

### <a name="application-store"></a><span data-ttu-id="6aeb8-110">Tienda de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6aeb8-110">Application Store</span></span>

<span data-ttu-id="6aeb8-111">Un instalador de aplicaciones registra una aplicación con PNM durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="6aeb8-111">An application installer registers an application with PNM during the installation process.</span></span> <span data-ttu-id="6aeb8-112">Estos son los objetos que pueden buscar otros usuarios al intentar conectarse a un usuario con una aplicación común, como un juego de equipos.</span><span class="sxs-lookup"><span data-stu-id="6aeb8-112">These are the objects that can be searched for by other users when attempting to connect to a user with a common application, such as a computer game.</span></span> <span data-ttu-id="6aeb8-113">Para cada aplicación, el almacén de aplicaciones contiene el nombre de la aplicación, un identificador único global (GUID), un ámbito de la aplicación, una descripción y una ruta de acceso al archivo ejecutable del programa.</span><span class="sxs-lookup"><span data-stu-id="6aeb8-113">For each application, the Application Store contains the name of the application, a globally unique identifier (GUID), a scope of the application, a description, and a path to the executable file of the program.</span></span> <span data-ttu-id="6aeb8-114">El ámbito de una aplicación se puede establecer en ninguno (no anunciado), equipos a mi alrededor (anunciado en la subred local), contactos (anunciados solo para contactos) o todo (anunciado en la subred local y para contactos).</span><span class="sxs-lookup"><span data-stu-id="6aeb8-114">The scope of an application can be set to None (not advertised), People Near Me (advertised on the local subnet), Contacts (advertised just for contacts), or All (advertised on the local subnet and for contacts).</span></span> <span data-ttu-id="6aeb8-115">El almacén de aplicaciones se encuentra en el registro de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6aeb8-115">The Application Store is located in the Windows Vista registry.</span></span>

 

 



