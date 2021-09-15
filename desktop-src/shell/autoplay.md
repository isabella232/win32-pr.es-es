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
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468304"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Creación de una aplicación de CD-ROM habilitada para ejecución automática

AutoRun es una característica del Windows operativo. Automatiza los procedimientos para instalar y configurar productos diseñados para Windows plataformas basadas en cd-ROMs. Cuando los usuarios insertan un disco compacto habilitado para ejecución automática en su unidad de CD-ROM, AutoRun ejecuta automáticamente una aplicación en el CD-ROM que instala, configura o ejecuta el producto seleccionado.

AutoRun se puede usar para instalar y ejecutar aplicaciones de CD-ROM. Aunque La ejecución automática se usa con más frecuencia para las aplicaciones de Windows, también se puede usar para instalar, configurar o ejecutar aplicaciones basadas en MS-DOS en una sesión de MS-DOS de Windows Microsoft. Puede configurar cada aplicación basada en MS-DOS con su propio icono único, Config.sys archivo y Autoexec.bat archivo. Windows crea los archivos de configuración correctos para la aplicación basada en MS-DOS. A continuación, la aplicación de inicio inicia la aplicación basada en MS-DOS en una ventana.

> [!Note]  
> Para que la ejecución automática funcione, la unidad de CD-ROM debe tener controladores de dispositivo de 32 o 64 bits que detecten cuándo un usuario inserta un disco compacto y notifica al sistema.

 

En las secciones siguientes se describe cómo implementar una aplicación de CD-ROM habilitada para ejecución automática.

-   [Creación de una AutoRun-Enabled aplicación](autoplay-works.md)
-   [Entradas autorun.inf](autorun-cmds.md)
-   [Habilitar y deshabilitar la ejecución automática](autoplay-reg.md)

 

 



