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
# <a name="establish-an-html-reference-to-setupexe"></a>Establecer una referencia HTML a Setup.exe

El paso final consiste en colocar una referencia al Setup.exe en la Página Web de instalación hipotética (MySetup.html) descrita en [una dirección URL basada Windows Installer ejemplo de instalación](a-url-based-windows-installer-installation-example.md). Use el siguiente script HTML:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Al hacer clic en el vínculo "instalación de", se muestra a los usuarios la opción de guardar o ejecutar desde esa ubicación. Si el usuario selecciona ejecutar desde esa ubicación, el Setup.exe actualiza la versión de Windows Installer en el equipo, si es necesario, comprueba la firma digital en el paquete del instalador e instala el paquete en su equipo.

Esto completa el ejemplo.

 

 



