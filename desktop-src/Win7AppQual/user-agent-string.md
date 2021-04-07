---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Cadena del agente de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003203"
---
# <a name="user-agent-string"></a><span data-ttu-id="59ab9-103">Cadena del agente de usuario</span><span class="sxs-lookup"><span data-stu-id="59ab9-103">User Agent String</span></span>

<span data-ttu-id="59ab9-104">La *cadena de agente de usuario* contiene información sobre la identidad de un explorador.</span><span class="sxs-lookup"><span data-stu-id="59ab9-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="59ab9-105">La cadena de agente de usuario se envía al servidor web como un encabezado HTTP cada vez que un explorador realiza una solicitud a un servidor Web.</span><span class="sxs-lookup"><span data-stu-id="59ab9-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="59ab9-106">También puede tener acceso a ella a través de un script del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="59ab9-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="59ab9-107">Por ejemplo, puede mostrar la cadena de agente de usuario escribiendo la siguiente dirección URL en la barra de direcciones de Windows Internet Explorer 8: "JavaScript: Alert (Navigator. userAgent)".</span><span class="sxs-lookup"><span data-stu-id="59ab9-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="59ab9-108">En la ilustración siguiente se muestra el cuadro de diálogo resultante típico de Internet Explorer 8 que se ejecuta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59ab9-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![captura de pantalla del cuadro diaog de Internet Explorer que tiene la cadena de agente de usuario](images/useragent-alert.png)

<span data-ttu-id="59ab9-110">Normalmente, la cadena de agente de usuario se analiza específicamente para la subcadena MSIE.</span><span class="sxs-lookup"><span data-stu-id="59ab9-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="59ab9-111">En función de la versión de detectada del explorador, la lógica de programación del lado cliente o del lado servidor toma una acción diferente.</span><span class="sxs-lookup"><span data-stu-id="59ab9-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="59ab9-112">Para obtener más información acerca de la cadena de agente de usuario, consulte [¿qué va a notificar Windows Internet Explorer como User-Agent cadena?](/previous-versions/cc817582(v=msdn.10)) en MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="59ab9-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59ab9-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59ab9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59ab9-114">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="59ab9-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



