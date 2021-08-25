---
title: Redistribución de software
description: Redistribución de software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows SDK de formato multimedia, redistribución de software
- Formato de sistemas avanzados (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- Windows SDK de formato multimedia, redistribución
- Formato de sistemas avanzados (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, acerca de
- redistribution,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b933df9319c342d8ed3502fc66757df2e6d8fd6e8d60309023ced6ffa042d5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807895"
---
# <a name="software-redistribution"></a>Redistribución de software

La inclusión de Windows de formato multimedia en una configuración de aplicación se conoce como redistribución. El SDK Windows Media Format incluye un paquete de instalación que se puede incluir con la configuración de la aplicación. El paquete de instalación es un archivo ejecutable denominado wmfdist95.exe. Al instalar el SDK de Windows Media Format, el paquete de instalación se copia en la carpeta Redist del directorio de instalación \\ (c: \\ wmsdk \\ wmfsdk de forma predeterminada).

En las secciones siguientes se proporcionan procedimientos y otra información para la configuración de redistribución de software.



| Sección                                                                            | Descripción                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Para crear una configuración de redistribución](to-create-a-redistribution-setup.md)           | Describe el procedimiento para crear una configuración de la aplicación.                                                                                                                       |
| [Detección del estado de la instalación](detecting-setup-status.md)                               | Proporciona código de ejemplo que comprueba el estado de instalación del Registro para determinar si es necesario instalar el paquete de redistribución.                                    |
| [Código de ejemplo para la configuración de redistribución](example-code-for-redistribution-setup.md) | Proporciona código de ejemplo que se puede usar en la rutina de instalación para ejecutar los paquetes de redistribución en modo silencioso y notificar a la rutina de instalación cuándo se debe reiniciar el equipo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Project Consideraciones**](project-considerations.md)
</dt> </dl>

 

 




