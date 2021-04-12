---
title: Acceso a bibliotecas
description: Acceso a bibliotecas
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, acceso
- Biblioteca, acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357072"
---
# <a name="library-access"></a><span data-ttu-id="d93e0-112">Acceso a bibliotecas</span><span class="sxs-lookup"><span data-stu-id="d93e0-112">Library Access</span></span>

<span data-ttu-id="d93e0-113">Las propiedades y los métodos del modelo de objetos de Media Player de Windows que tienen acceso a la biblioteca requieren acceso de solo lectura o de lectura y escritura a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d93e0-113">Properties and methods of the Windows Media Player object model that access the library require either read-only or read/write access to the database.</span></span> <span data-ttu-id="d93e0-114">La biblioteca contiene información que algunos usuarios quieren mantener privados y a los que se debe tener acceso o modificar solo con su consentimiento.</span><span class="sxs-lookup"><span data-stu-id="d93e0-114">The library contains information that some users want to keep private and that should be accessed or altered only with their consent.</span></span>

<span data-ttu-id="d93e0-115">En Windows Media Player serie 9 o posterior, puede determinar mediante programación el nivel de acceso.</span><span class="sxs-lookup"><span data-stu-id="d93e0-115">For Windows Media Player 9 Series or later, you can programmatically determine access level.</span></span> <span data-ttu-id="d93e0-116">Para determinar el nivel actual de acceso concedido al código, recupere la *configuración*. propiedad **mediaAccessRights** .</span><span class="sxs-lookup"><span data-stu-id="d93e0-116">To determine the current level of access granted to your code, retrieve the *Settings*.**mediaAccessRights** property.</span></span> <span data-ttu-id="d93e0-117">Esa propiedad devuelve "none", "Read" o "Full" (lectura y escritura).</span><span class="sxs-lookup"><span data-stu-id="d93e0-117">That property returns "none", "read", or "full" (read/write).</span></span> <span data-ttu-id="d93e0-118">Para solicitar derechos de acceso específicos, llame a la *configuración*. método **requestMediaAccessRights** , pasando un parámetro que especifica el nivel que se solicita.</span><span class="sxs-lookup"><span data-stu-id="d93e0-118">To request specific access rights, call the *Settings*.**requestMediaAccessRights** method, passing a parameter that specifies the level you are requesting.</span></span> <span data-ttu-id="d93e0-119">El método muestra un mensaje al usuario que explica el nivel de acceso solicitado y devuelve un valor **booleano** que indica si se ha concedido el acceso.</span><span class="sxs-lookup"><span data-stu-id="d93e0-119">The method displays a message to the user explaining the requested level of access, and returns a **Boolean** value indicating whether the access was granted.</span></span>

<span data-ttu-id="d93e0-120">Determinados derechos de acceso se conceden automáticamente en función de dónde se ejecute el código en relación con el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="d93e0-120">Certain access rights are granted automatically depending on where your code is running relative to the user's computer.</span></span>

-   <span data-ttu-id="d93e0-121">Si la página web o el programa se encuentra en el equipo del usuario, se concederán derechos de acceso completo de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d93e0-121">If your webpage or program is located on the user's computer, full access rights are granted by default.</span></span>
-   <span data-ttu-id="d93e0-122">Las páginas web tienen acceso de lectura al *reproductor*. **currentMedia**, *reproductor*. **currentPlaylist** y *multimedia*. **sourceURL** cuando la página web se encuentra en una zona de seguridad de Internet Explorer que es igual o menos restringida que la zona de seguridad del elemento multimedia o de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d93e0-122">Web pages have read access to *Player*.**currentMedia**, *Player*.**currentPlaylist**, and *Media*.**sourceURL** when the webpage is located in an Internet Explorer security zone that is the same as or less restricted than the security zone of the media item or playlist.</span></span>

    <span data-ttu-id="d93e0-123">En el intervalo de menos restringido a más restringido, las zonas de seguridad son la zona de **confianza** (incluido el equipo local del usuario), la zona de **Intranet local** , la zona de **Internet** y la zona **restringida** .</span><span class="sxs-lookup"><span data-stu-id="d93e0-123">Ranging from least restricted to most restricted, the security zones are the **Trusted** zone (including the user's local computer), the **Local intranet** zone, the **Internet** zone, and the **Restricted** zone.</span></span>

    <span data-ttu-id="d93e0-124">Por ejemplo, una página web de la zona **Intranet local** tiene derechos de acceso completo al *reproductor*. **currentMedia** cuando el elemento multimedia correspondiente está en la Intranet local o en Internet, pero se deben solicitar derechos de acceso para los elementos multimedia ubicados en el equipo local de un usuario o en un sitio web de la zona de **confianza** .</span><span class="sxs-lookup"><span data-stu-id="d93e0-124">For example, a webpage in the **Local intranet** zone has full access rights to *Player*.**currentMedia** when the corresponding media item is on the local intranet or the Internet, but access rights must be requested for media items located on a user's local computer or on a website in the **Trusted** zone.</span></span>

<span data-ttu-id="d93e0-125">Debe probar la aplicación basada en web o en Windows en todas las zonas de seguridad con las que puede encontrarse.</span><span class="sxs-lookup"><span data-stu-id="d93e0-125">You should test your Web-based or Windows-based application in all of the security zones it may encounter.</span></span> <span data-ttu-id="d93e0-126">La aplicación debe diseñarse para controlar la denegación de una solicitud de acceso correctamente.</span><span class="sxs-lookup"><span data-stu-id="d93e0-126">The application should be designed to handle denial of an access request correctly.</span></span>

<span data-ttu-id="d93e0-127">Las versiones del modelo de objetos de Windows Media Player anteriores a Windows Media Player 9 no incluyen **mediaAccessRights** ni **requestMediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="d93e0-127">Windows Media Player object model versions prior to Windows Media Player 9 Series do not include **mediaAccessRights** or **requestMediaAccessRights**.</span></span> <span data-ttu-id="d93e0-128">Estas versiones anteriores de Windows Media Player permiten al usuario establecer niveles de acceso mediante el cuadro de diálogo **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="d93e0-128">These earlier versions of Windows Media Player enable the user to set access levels using the **Options** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d93e0-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d93e0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d93e0-130">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="d93e0-130">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="d93e0-131">**Trabajar con la biblioteca**</span><span class="sxs-lookup"><span data-stu-id="d93e0-131">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




