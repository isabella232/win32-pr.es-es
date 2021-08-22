---
description: AutoRun es una característica del Windows operativo.
title: Creación de una aplicación de CD-ROM habilitada para ejecución automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b8bc1edad7fe49b996dd8471ae8ce081c36c71b7b7df48ca6296b07f8646ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460935"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Creación de una aplicación de CD-ROM habilitada para ejecución automática

AutoRun es una característica del Windows operativo. Automatiza los procedimientos para instalar y configurar productos diseñados para Windows plataformas basadas en cd-roms que se distribuyen en CD-ROMs. Cuando los usuarios insertan un disco compacto habilitado para ejecución automática en su unidad de CD-ROM, AutoRun ejecuta automáticamente una aplicación en el CD-ROM que instala, configura o ejecuta el producto seleccionado.

AutoRun se puede usar para instalar y ejecutar aplicaciones de CD-ROM. Aunque La ejecución automática se usa con más frecuencia para las aplicaciones de Windows, también se puede usar para instalar, configurar o ejecutar aplicaciones basadas en MS-DOS en una Windows de Microsoft MS-DOS. Puede configurar cada aplicación basada en MS-DOS con su propio icono único, Config.sys archivo y Autoexec.bat archivo. Windows crea los archivos de configuración correctos para la aplicación basada en MS-DOS. A continuación, la aplicación de inicio inicia la aplicación basada en MS-DOS en una ventana.

> [!Note]  
> Para que la ejecución automática funcione, la unidad de CD-ROM debe tener controladores de dispositivo de 32 o 64 bits que detecten cuándo un usuario inserta un disco compacto y notifica al sistema.

 

En las secciones siguientes se describe cómo implementar una aplicación de CD-ROM habilitada para ejecución automática.

-   [Creación de una AutoRun-Enabled aplicación](autoplay-works.md)
-   [Entradas autorun.inf](autorun-cmds.md)
-   [Habilitación y deshabilitación de autorun](autoplay-reg.md)

 

 



