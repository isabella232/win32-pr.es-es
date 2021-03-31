---
description: El paso final consiste en colocar una referencia al Setup.exe en la Página Web de instalación hipotética (MySetup.html) descrita en una dirección URL basada Windows Installer ejemplo de instalación.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Establecer una referencia HTML a Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277175"
---
# <a name="establish-an-html-reference-to-setupexe"></a><span data-ttu-id="1f45c-103">Establecer una referencia HTML a Setup.exe</span><span class="sxs-lookup"><span data-stu-id="1f45c-103">Establish an HTML Reference to Setup.exe</span></span>

<span data-ttu-id="1f45c-104">El paso final consiste en colocar una referencia al Setup.exe en la Página Web de instalación hipotética (MySetup.html) descrita en [una dirección URL basada Windows Installer ejemplo de instalación](a-url-based-windows-installer-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="1f45c-104">The final step is to place a reference to the Setup.exe on the hypothetical MySetup webpage (MySetup.html) described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span> <span data-ttu-id="1f45c-105">Use el siguiente script HTML:</span><span class="sxs-lookup"><span data-stu-id="1f45c-105">Use the following HTML script:</span></span>

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

<span data-ttu-id="1f45c-106">Al hacer clic en el vínculo "instalación de", se muestra a los usuarios la opción de guardar o ejecutar desde esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="1f45c-106">Clicking on the "MySetup Installation" link presents users with the option to save or run from that location.</span></span> <span data-ttu-id="1f45c-107">Si el usuario selecciona ejecutar desde esa ubicación, el Setup.exe actualiza la versión de Windows Installer en el equipo, si es necesario, comprueba la firma digital en el paquete del instalador e instala el paquete en su equipo.</span><span class="sxs-lookup"><span data-stu-id="1f45c-107">If the user selects run from that location, the Setup.exe upgrades the version of Windows Installer on the computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>

<span data-ttu-id="1f45c-108">Esto completa el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1f45c-108">This completes the example.</span></span>

 

 



