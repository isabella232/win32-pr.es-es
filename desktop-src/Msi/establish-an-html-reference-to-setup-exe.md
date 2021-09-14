---
description: El paso final consiste en colocar una referencia a Setup.exe en la página web hipotética de MySetup (MySetup.html) descrita en A URL Based Windows Installer Installation Example (Ejemplo de instalación del instalador de Windows URL).
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Establecer una referencia HTML para Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158448"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Establecer una referencia HTML para Setup.exe

El paso final consiste en colocar una referencia a Setup.exe en la página web hipotética de MySetup (MySetup.html) descrita en [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md). Use el siguiente script HTML:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Al hacer clic en el vínculo "Instalación de MySetup", los usuarios tienen la opción de guardar o ejecutar desde esa ubicación. Si el usuario selecciona ejecutar desde esa ubicación, Setup.exe actualiza la versión de Windows Installer en el equipo, si es necesario, comprueba la firma digital en el paquete del instalador e instala el paquete en su equipo.

Esto completa el ejemplo.

 

 



