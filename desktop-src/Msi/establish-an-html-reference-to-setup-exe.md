---
description: El paso final consiste en colocar una referencia a la Setup.exe en la página web hipotética de MySetup (MySetup.html) descrita en A URL Based Windows Installer Installation Example (Ejemplo de instalación de un instalador basado en una dirección URL).
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Establecer una referencia HTML para Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22be693c4e2e411fa724a70f90da4af4af4cf17ad6bb316bd3a483dd55bfd5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378075"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Establecer una referencia HTML para Setup.exe

El paso final consiste en colocar una referencia a Setup.exe en la página web hipotética de MySetup (MySetup.html) descrita en A [URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md). Use el siguiente script HTML:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Al hacer clic en el vínculo "Instalación de MySetup", los usuarios tienen la opción de guardar o ejecutar desde esa ubicación. Si el usuario selecciona ejecutar desde esa ubicación, el Setup.exe actualiza la versión de Windows Installer en el equipo, si es necesario, comprueba la firma digital en el paquete del instalador e instala el paquete en su equipo.

Esto completa el ejemplo.

 

 



