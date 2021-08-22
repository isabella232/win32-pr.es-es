---
title: Acceso al control desde Visual Basic y otros lenguajes de programación
description: Acceso al control desde Visual Basic y otros lenguajes de programación
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fe0c5e7548283a84edff1fb3ded488c1367087e12c15d1578629ce80b51297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976865"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Acceso al control desde Visual Basic y otros lenguajes de programación

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

También puede usar el control de Microsoft Agent desde Visual Basic otros lenguajes de programación. Asegúrese de que el lenguaje es totalmente compatible con ActiveX interfaz de control y siga sus convenciones para agregar y acceder a ActiveX controles. Para acceder al control , el Agente ya debe estar instalado en el sistema de destino.

A continuación, puede descargar el archivo de archivador de instalación automática del Agente desde el sitio web (mediante la opción Guardar en lugar de ejecutar). Puede incluir este archivo en el programa de instalación. Cada vez que se ejecute, instalará automáticamente el Agente en el sistema de destino. Para más información sobre la instalación, consulte el contrato de licencia de distribución de Microsoft Agent. No se admite la instalación que no sea el archivo de archivador auto-instalación del Agente , como el intento de copiar y registrar archivos de componentes del Agente . Esto garantiza una instalación coherente y completa. Tenga en cuenta que el archivo de instalación propia de Microsoft Agent no se instalará en Microsoft Windows 2000 porque esa versión del sistema operativo ya incluye su propia versión del Agente .

Para instalar correctamente el Agente en un sistema de destino, también debe asegurarse de que el sistema de destino tiene una versión reciente del entorno de ejecución de Microsoft Visual C++ (Msvcrt.dll), la herramienta de registro de Microsoft (Regsvr32.dll) y los archivos DLL COM de Microsoft. La manera más fácil de asegurarse de que los componentes necesarios están en el sistema de destino es requerir que Microsoft Internet Explorer 3.02 o posterior esté instalado. Como alternativa, puede instalar los dos primeros componentes que están disponibles como parte de Microsoft Visual C++. Los archivos DLL COM necesarios se pueden instalar como parte de la actualización de Microsoft DCOM, disponible en el sitio web de Microsoft. Puede encontrar más información e información sobre licencias para estos componentes en el sitio web de Microsoft.

Los componentes de lenguaje del agente se pueden instalar de la misma manera. De forma similar, puede usar esta técnica para instalar el formato ACS de los caracteres de Microsoft disponibles para su distribución desde el sitio web de Microsoft Agent. Los archivos de caracteres se instalan automáticamente en el \\ subdirectorio Chars del agente de Microsoft.

Dado que los componentes de Microsoft Agent están diseñados como componentes del sistema operativo, es posible que el Agente no se desinstale. Del mismo modo, si el Agente ya está instalado como parte del sistema operativo Windows, es posible que el gabinete auto-instalación del Agente no se instale.

 

 




