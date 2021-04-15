---
title: Acceder al control desde Visual Basic y otros lenguajes de programación
description: Acceder al control desde Visual Basic y otros lenguajes de programación
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45854b55b3826354543411c44dcd21d9f1d77e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695394"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Acceder al control desde Visual Basic y otros lenguajes de programación

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

También puede utilizar el control de Microsoft Agent desde Visual Basic y otros lenguajes de programación. Asegúrese de que el lenguaje sea totalmente compatible con la interfaz de control ActiveX y siga las convenciones para agregar y obtener acceso a los controles ActiveX. Para tener acceso al control, el agente ya debe estar instalado en el sistema de destino.

Después, puede descargar el archivo. cab de instalación automática del agente desde el sitio web (mediante la opción Guardar en lugar de ejecutar). Puede incluir este archivo en el programa de instalación de la instalación de. Cada vez que se ejecuta, se instalará automáticamente el agente en el sistema de destino. Para más información sobre la instalación, consulte el contrato de licencia de distribución de Microsoft Agent. No se admite la instalación que no sea mediante el archivo contenedor de instalación automática del agente, como el intento de copiar y registrar archivos de componente de agente. Esto garantiza una instalación coherente y completa. Tenga en cuenta que el archivo de instalación automática de Microsoft Agent no se instalará en Microsoft Windows 2000 porque la versión del sistema operativo ya incluye su propia versión del agente.

Para instalar correctamente el agente en un sistema de destino, también debe asegurarse de que el sistema de destino tiene una versión reciente del tiempo de ejecución de Microsoft Visual C++ (Msvcrt.dll), la herramienta de registro de Microsoft (Regsvr32.dll) y los archivos dll de Microsoft COM. La manera más sencilla de asegurarse de que los componentes necesarios están en el sistema de destino es requerir la instalación de Microsoft Internet Explorer 3,02 o posterior. Como alternativa, puede instalar los dos primeros componentes que están disponibles como parte de Microsoft Visual C++. Los archivos DLL COM necesarios se pueden instalar como parte de la actualización DCOM de Microsoft, disponible en el sitio web de Microsoft. Puede encontrar más información e información de licencia para estos componentes en el sitio web de Microsoft.

Los componentes de idioma del agente se pueden instalar de la misma manera. De forma similar, puede usar esta técnica para instalar el formato de ACS de los caracteres de Microsoft disponibles para la distribución desde el sitio web del agente de Microsoft. Los archivos de caracteres se instalan automáticamente en el subdirectorio de caracteres del agente de Microsoft \\ .

Dado que los componentes de Microsoft Agent están diseñados como componentes del sistema operativo, es posible que el agente no se desinstale. Del mismo modo, si el agente ya está instalado como parte del sistema operativo Windows, es posible que el archivo. cab de instalación automática del agente no se instale.

 

 




