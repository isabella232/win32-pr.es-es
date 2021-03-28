---
description: La ejecución automática es una característica del sistema operativo Windows.
title: Creación de una aplicación de CD-ROM habilitada para AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275250"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Creación de una aplicación de CD-ROM habilitada para AutoRun

La ejecución automática es una característica del sistema operativo Windows. Automatiza los procedimientos para instalar y configurar productos diseñados para plataformas basadas en Windows que se distribuyen en CD-ROM. Cuando los usuarios insertan un disco compacto habilitado para la ejecución automática en la unidad de CD-ROM, el programa de ejecución automática ejecuta automáticamente una aplicación en el CD-ROM que instala, configura o ejecuta el producto seleccionado.

La ejecución automática se puede usar para instalar y ejecutar aplicaciones de CD-ROM. Aunque la ejecución automática se usa normalmente para las aplicaciones Windows, también se puede usar para instalar, configurar o ejecutar aplicaciones basadas en MS-DOS en una sesión de Microsoft MS-DOS. Puede configurar cada aplicación basada en MS-DOS con su propio icono único, Config.sys archivo y Autoexec.bat archivo. Windows crea los archivos de configuración correctos para la aplicación basada en MS-DOS. A continuación, la aplicación de inicio inicia la aplicación basada en MS-dos en una ventana de.

> [!Note]  
> Para que la ejecución automática funcione, la unidad de CD-ROM debe tener controladores de dispositivos de 32 o 64 bits que detecten Cuándo un usuario inserta un disco compacto y notifica al sistema.

 

En las secciones siguientes se describe cómo implementar una aplicación de CD-ROM habilitada para AutoRun.

-   [Creación de una aplicación AutoRun-Enabled](autoplay-works.md)
-   [Entradas Autorun. inf](autorun-cmds.md)
-   [Habilitar y deshabilitar la ejecución automática](autoplay-reg.md)

 

 



