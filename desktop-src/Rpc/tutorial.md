---
title: Tutorial
description: Este tutorial le guiará por los pasos necesarios para crear una aplicación distribuida simple de un solo cliente y de un solo servidor a partir de una aplicación independiente existente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC llamada a procedimiento remoto, tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076087"
---
# <a name="tutorial"></a><span data-ttu-id="7dcdf-104">Tutorial</span><span class="sxs-lookup"><span data-stu-id="7dcdf-104">Tutorial</span></span>

<span data-ttu-id="7dcdf-105">Este tutorial le guiará por los pasos necesarios para crear una aplicación distribuida simple de un solo cliente y de un solo servidor a partir de una aplicación independiente existente.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-105">This tutorial takes you through the steps required to create a simple, single-client, single-server distributed application from an existing standalone application.</span></span> <span data-ttu-id="7dcdf-106">Los pasos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7dcdf-106">These steps are:</span></span>

-   <span data-ttu-id="7dcdf-107">Crear definición de interfaz y archivos de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-107">Create interface definition and application configuration files.</span></span>
-   <span data-ttu-id="7dcdf-108">Utilice el compilador MIDL para generar el código auxiliar y los encabezados de cliente y servidor de lenguaje C a partir de esos archivos.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-108">Use the MIDL compiler to generate C-language client and server stubs and headers from those files.</span></span>
-   <span data-ttu-id="7dcdf-109">Escriba una aplicación cliente que administre su conexión con el servidor de.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-109">Write a client application that manages its connection to the server.</span></span>
-   <span data-ttu-id="7dcdf-110">Escriba una aplicación de servidor que contenga los procedimientos remotos reales.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-110">Write a server application that contains the actual remote procedures.</span></span>
-   <span data-ttu-id="7dcdf-111">Compile y vincule estos archivos a la biblioteca en tiempo de ejecución de RPC para generar la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-111">Compile and link these files to the RPC run-time library to produce the distributed application.</span></span>

<span data-ttu-id="7dcdf-112">La aplicación cliente pasa una cadena de caracteres al servidor en una llamada a procedimiento remoto y el servidor imprime la cadena "Hello, World" en la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-112">The client application passes a character string to the server in a remote procedure call, and the server prints the string "Hello, World" to its standard output.</span></span>

<span data-ttu-id="7dcdf-113">Los archivos de código fuente completos para esta aplicación de ejemplo, con código adicional para controlar la entrada de la línea de comandos y enviar varios mensajes de estado al usuario, se encuentran en el \\ Directorio de RPC Hola del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="7dcdf-113">The complete source files for this example application, with additional code to handle command-line input and to output various status messages to the user, are in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="7dcdf-114">En esta sección se presenta su debate en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="7dcdf-114">This section presents its discussion in the following topics:</span></span>

-   [<span data-ttu-id="7dcdf-115">Aplicación independiente</span><span class="sxs-lookup"><span data-stu-id="7dcdf-115">The Standalone Application</span></span>](the-standalone-application.md)
-   [<span data-ttu-id="7dcdf-116">Definir la interfaz</span><span class="sxs-lookup"><span data-stu-id="7dcdf-116">Defining the Interface</span></span>](defining-the-interface.md)
-   [<span data-ttu-id="7dcdf-117">Generar el UUID</span><span class="sxs-lookup"><span data-stu-id="7dcdf-117">Generating the UUID</span></span>](generating-the-uuid.md)
-   [<span data-ttu-id="7dcdf-118">El archivo IDL</span><span class="sxs-lookup"><span data-stu-id="7dcdf-118">The IDL File</span></span>](the-idl-file.md)
-   [<span data-ttu-id="7dcdf-119">El archivo ACF</span><span class="sxs-lookup"><span data-stu-id="7dcdf-119">The ACF File</span></span>](the-acf-file.md)
-   [<span data-ttu-id="7dcdf-120">Generar archivos de código auxiliar</span><span class="sxs-lookup"><span data-stu-id="7dcdf-120">Generating the Stub Files</span></span>](generating-the-stub-files.md)
-   [<span data-ttu-id="7dcdf-121">La aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="7dcdf-121">The Client Application</span></span>](the-client-application.md)
-   [<span data-ttu-id="7dcdf-122">La aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="7dcdf-122">The Server Application</span></span>](the-server-application.md)
-   [<span data-ttu-id="7dcdf-123">Detener la aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="7dcdf-123">Stopping the Server Application</span></span>](stopping-the-server-application.md)
-   [<span data-ttu-id="7dcdf-124">Compilar y vincular</span><span class="sxs-lookup"><span data-stu-id="7dcdf-124">Compiling and Linking</span></span>](compiling-and-linking.md)
-   [<span data-ttu-id="7dcdf-125">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="7dcdf-125">Running the Application</span></span>](running-the-application.md)

 

 




