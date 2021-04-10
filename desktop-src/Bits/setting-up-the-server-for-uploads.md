---
title: Configuración del servidor para cargas
description: Para cargar archivos en un servidor mediante BITS, el servidor debe tener instalado IIS y la extensión de servidor BITS ISAPI. Para conocer los requisitos de IIS, consulte requisitos de IIS para cargas de BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268315"
---
# <a name="setting-up-the-server-for-uploads"></a><span data-ttu-id="61bc5-104">Configuración del servidor para cargas</span><span class="sxs-lookup"><span data-stu-id="61bc5-104">Setting Up the Server for Uploads</span></span>

<span data-ttu-id="61bc5-105">Para cargar archivos en un servidor mediante BITS, el servidor debe tener instalado IIS y la extensión de servidor BITS ISAPI.</span><span class="sxs-lookup"><span data-stu-id="61bc5-105">To upload files to a server using BITS, the server must have IIS and the BITS server extension ISAPI installed.</span></span> <span data-ttu-id="61bc5-106">Para conocer los requisitos de IIS, consulte [requisitos de IIS para cargas de bits](iis-requirements-for-bits-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="61bc5-106">For IIS requirements, see [IIS Requirements for BITS Uploads](iis-requirements-for-bits-uploads.md).</span></span>

<span data-ttu-id="61bc5-107">Para obtener información sobre la configuración del directorio virtual de IIS que usa BITS para cargas, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="61bc5-107">For information on configuring the IIS virtual directory that BITS uses for uploads, see the following topics.</span></span>

-   [<span data-ttu-id="61bc5-108">Establecimiento de permisos en directorios virtuales</span><span class="sxs-lookup"><span data-stu-id="61bc5-108">Setting Permissions on Virtual Directories</span></span>](setting-permissions-on-virtual-directories.md)
-   [<span data-ttu-id="61bc5-109">Escritura de un script para configurar el directorio virtual</span><span class="sxs-lookup"><span data-stu-id="61bc5-109">Writing a Script to Configure the Virtual Directory</span></span>](writing-a-script-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="61bc5-110">Usar la interfaz de usuario de IIS para configurar el directorio virtual</span><span class="sxs-lookup"><span data-stu-id="61bc5-110">Using the IIS UI to Configure the Virtual Directory</span></span>](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="61bc5-111">Impedir varias cargas</span><span class="sxs-lookup"><span data-stu-id="61bc5-111">Preventing Multiple Uploads</span></span>](preventing-multiple-uploads.md)
-   [<span data-ttu-id="61bc5-112">Procedimientos recomendados de carga</span><span class="sxs-lookup"><span data-stu-id="61bc5-112">Upload Best Practices</span></span>](upload-best-practices.md)

> [!Note]  
> <span data-ttu-id="61bc5-113">Algunas instalaciones de IIS incluyen el componente de filtrado UrlScan.</span><span class="sxs-lookup"><span data-stu-id="61bc5-113">Some IIS installations include the UrlScan filtering component.</span></span> <span data-ttu-id="61bc5-114">Si UrlScan está habilitado, el administrador debe agregar el verbo "BITS \_ post" a la lista de verbos http permitidos de URLScan.</span><span class="sxs-lookup"><span data-stu-id="61bc5-114">If UrlScan is enabled, the administrator must add the "BITS\_POST" verb to UrlScan's list of allowed HTTP verbs.</span></span> <span data-ttu-id="61bc5-115">De lo contrario, se producirá un error en las cargas del cliente de BITS.</span><span class="sxs-lookup"><span data-stu-id="61bc5-115">Otherwise, BITS client uploads will fail.</span></span> <span data-ttu-id="61bc5-116">Para obtener más información sobre cómo habilitar verbos en UrlScan, vea la documentación de UrlScan.</span><span class="sxs-lookup"><span data-stu-id="61bc5-116">For further details on enabling verbs in UrlScan, see the UrlScan documentation.</span></span>

 

 

 




