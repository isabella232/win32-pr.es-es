---
description: Puede depurar acciones personalizadas basadas en bibliotecas de vínculos dinámicos mediante herramientas de depuración para Windows. No es posible usar la depuración dinámica con acciones personalizadas basadas en archivos ejecutables o scripts.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Depuración de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ddfbc9952f0dd7fc1b85b5c64fa6a23381ceafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667810"
---
# <a name="debugging-custom-actions"></a>Depuración de acciones personalizadas

Puede depurar acciones personalizadas basadas en [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) mediante [herramientas de depuración para Windows](https://www.microsoft.com/?ref=go). No es posible usar la depuración dinámica con acciones personalizadas basadas en [archivos ejecutables](executable-files.md) o [scripts](scripts.md).

Las técnicas descritas en esta sección pueden ayudarle a depurar Windows Installer acciones personalizadas. Consulte la sección herramientas de desarrollo de controladores de Windows Driver Kit (WDK) para obtener información sobre [las herramientas de depuración para Windows](https://www.microsoft.com/?ref=go).

Windows Installer usa la variable de entorno MsiBreak para determinar la acción personalizada que se va a depurar. Si tiene acceso al código fuente de la acción personalizada, es posible que pueda usar la depuración sin MsiBreak. Para iniciar la depuración sin MsiBreak, coloque un cuadro de mensaje temporal al principio del código de la acción. Cuando aparezca el cuadro de mensaje durante la instalación, adjunte el depurador al proceso que posee el cuadro de mensaje. Después, puede establecer los puntos de interrupción necesarios y descartar el cuadro de mensaje para reanudar la ejecución. Este método no puede depurar las partes anteriores de la acción personalizada.

Para usar la variable de entorno MsiBreak para depurar la acción personalizada, establezca MsiBreak en el nombre de la acción personalizada en la [tabla CustomAction](customaction-table.md). MsiBreak puede ser una variable de entorno de sistema o de usuario. Si la variable se establece como una variable del sistema, es posible que sea necesario reiniciar el sistema cuando se cambie el valor para detectar el nuevo valor.

Para usar la variable de entorno MsiBreak para depurar una interfaz de usuario incrustada, establezca el valor de MsiBreak en MsiEmbeddedUI.

Windows Installer solo comprueba la variable de entorno MsiBreak si el usuario es un administrador. El instalador omite el valor de MsiBreak si el usuario no es un administrador, aunque se trata de una [*aplicación administrada*](m-gly.md).

Si está depurando una acción personalizada que se ejecuta con privilegios elevados (del sistema) en la secuencia de ejecución, asocie el depurador al servicio Windows Installer. Al depurar una acción personalizada que se ejecuta con privilegios suplantados en la secuencia de ejecución, el sistema solicita un cuadro de diálogo que indica qué proceso se debe depurar. Se muestra al usuario un cuadro de diálogo que indica el proceso que se va a depurar. Para obtener más información sobre las acciones personalizadas elevadas, vea seguridad de la [acción personalizada](custom-action-security.md).

Una vez que el depurador se ha adjuntado al proceso correcto, el instalador desencadena un punto de interrupción del depurador inmediatamente antes de llamar al punto de entrada del archivo DLL. En el punto de interrupción, el archivo DLL ya está cargado en el proceso y se ha determinado la dirección del punto de entrada. Si no se pudo cargar el archivo DLL de acción personalizada o no existe el punto de entrada de la acción personalizada, no se desencadena ningún punto de interrupción. Dado que el punto de interrupción se desencadena antes de llamar a la función DLL, una vez que se ha desencadenado el punto de interrupción, se debe usar el depurador para avanzar hasta que se llame al punto de entrada de la acción personalizada. Como alternativa, puede establecer un punto de interrupción en cualquier parte de la acción personalizada y reanudar la ejecución normal.

El Windows Installer ejecuta archivos dll no almacenados en la [tabla binaria](binary-table.md) directamente desde la ubicación del archivo dll. El instalador no conoce el nombre original de un archivo DLL almacenado en la tabla binaria y ejecuta la acción personalizada DLL bajo un nombre de archivo temporal. El formato del nombre de archivo temporal es MSI?????. Gestión. En Windows XP, este archivo temporal se almacena en una ubicación segura, normalmente en el <WindowFolder> \\ instalador.

Tenga en cuenta que muchos archivos dll creados para depuración contienen el nombre y la ruta de acceso del archivo PDB correspondiente como parte del propio archivo DLL. Al depurar este tipo de archivo DLL en un sistema en el que se puede encontrar la PDB en la ubicación almacenada en el archivo DLL, la herramienta de depurador puede cargar símbolos automáticamente. En situaciones en las que el archivo PDB no puede encontrarse en la ubicación almacenada, donde el depurador no admite la carga de símbolos desde la ubicación almacenada o donde la DLL no se compiló con información de depuración, puede que tenga que colocar los archivos de símbolos en la carpeta con el archivo DLL temporal.

El instalador agrega información de depuración para los scripts de acción personalizada al archivo de registro de instalación.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



