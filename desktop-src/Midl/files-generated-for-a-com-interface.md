---
title: Archivos generados para una interfaz COM
description: En el caso de las interfaces COM, el compilador MIDL combina todas las rutinas y datos auxiliares del servidor de objetos y cliente en un único archivo proxy de interfaz.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL del compilador MIDL, MIDL y COM
- MIDL EN COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995179"
---
# <a name="files-generated-for-a-com-interface"></a><span data-ttu-id="7f476-105">Archivos generados para una interfaz COM</span><span class="sxs-lookup"><span data-stu-id="7f476-105">Files Generated for a COM Interface</span></span>

<span data-ttu-id="7f476-106">En el caso de las interfaces COM, el compilador MIDL combina todas las rutinas y datos auxiliares del servidor de objetos y cliente en un único archivo proxy de interfaz.</span><span class="sxs-lookup"><span data-stu-id="7f476-106">For COM interfaces, the MIDL compiler combines all client and object server auxiliary routines and data into a single interface proxy file.</span></span> <span data-ttu-id="7f476-107">Este archivo incluye los puntos de entrada suplente para clientes y servidores.</span><span class="sxs-lookup"><span data-stu-id="7f476-107">This file includes the surrogate entry points for both clients and servers.</span></span> <span data-ttu-id="7f476-108">Además, el compilador MIDL genera un archivo de encabezado de interfaz, un archivo UUID de interfaz y un archivo de registro de interfaz.</span><span class="sxs-lookup"><span data-stu-id="7f476-108">In addition, the MIDL compiler generates an interface header file, an interface UUID file and an interface registration file.</span></span> <span data-ttu-id="7f476-109">Usará todos estos archivos al crear un archivo DLL de proxy que contenga el código para admitir el uso de la interfaz por parte de las aplicaciones cliente y los servidores de objetos.</span><span class="sxs-lookup"><span data-stu-id="7f476-109">You will use all these files when creating a proxy DLL that contains the code to support the use of the interface by both client applications and object servers.</span></span> <span data-ttu-id="7f476-110">También usará el archivo de encabezado de interfaz y el archivo UUID de interfaz al crear el archivo ejecutable para una aplicación cliente que use la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7f476-110">You will also use the interface header file and the interface UUID file when creating the executable file for a client application that uses the interface.</span></span>

<span data-ttu-id="7f476-111">En los temas siguientes se describe cada uno de los archivos generados para una interfaz COM personalizada, que se identifican mediante la inclusión del **\[** [](object.md) **\]** atributo de objeto en la lista de atributos de interfaz del archivo IDL:</span><span class="sxs-lookup"><span data-stu-id="7f476-111">The following topics describe each of the files generated for a custom COM interface, which you identify by including the **\[**[**object**](object.md)**\]** attribute in the interface attribute list of the IDL file:</span></span>

-   [<span data-ttu-id="7f476-112">El archivo de proxy de interfaz</span><span class="sxs-lookup"><span data-stu-id="7f476-112">The Interface Proxy File</span></span>](the-interface-proxy-file.md)
-   [<span data-ttu-id="7f476-113">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7f476-113">The Header Files</span></span>](the-header-files.md)
-   [<span data-ttu-id="7f476-114">El archivo UUID de la interfaz</span><span class="sxs-lookup"><span data-stu-id="7f476-114">The Interface UUID File</span></span>](the-interface-uuid-file.md)
-   [<span data-ttu-id="7f476-115">El archivo de registro de la interfaz</span><span class="sxs-lookup"><span data-stu-id="7f476-115">The Interface Registration File</span></span>](the-interface-registration-file.md)

<span data-ttu-id="7f476-116">Para obtener más información, consulte archivo de configuración de la [aplicación (ACF)](application-configuration-file-acf-.md), [**/App \_ config**](-app-config.md), [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)y [compilar y registrar un archivo dll de proxy](../com/building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="7f476-116">For more information, see [Application Configuration File (ACF)](application-configuration-file-acf-.md), [**/app\_config**](-app-config.md), [Interface Definition (IDL) File](interface-definition-idl-file.md), and [Building and Registering a Proxy DLL](../com/building-and-registering-a-proxy-dll.md).</span></span>

 

 