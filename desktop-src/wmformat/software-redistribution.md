---
title: Redistribución de software
description: Redistribución de software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- SDK de Windows Media Format, redistribución de software
- Advanced Systems Format (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- SDK de Windows Media Format, redistribución
- Advanced Systems Format (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, acerca de
- redistribución, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775012"
---
# <a name="software-redistribution"></a>Redistribución de software

La inclusión del software Windows Media Format en una configuración de aplicación se conoce como redistribución. El SDK de Windows Media Format incluye un paquete de instalación que se puede incluir con la configuración de la aplicación. El paquete de instalación es un archivo ejecutable denominado wmfdist95.exe. Al instalar el SDK de Windows Media Format, el paquete de instalación se copia en la \\ carpeta Redist del directorio de instalación (c: \\ wmsdk wmfsdk de \\ forma predeterminada).

En las secciones siguientes se proporcionan procedimientos y otra información para la configuración de la redistribución de software.



| Sección                                                                            | Descripción                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Para crear una configuración de redistribución](to-create-a-redistribution-setup.md)           | Describe el procedimiento para crear una instalación de la aplicación.                                                                                                                       |
| [Detección del estado de la instalación](detecting-setup-status.md)                               | Proporciona código de ejemplo que comprueba el estado de la instalación del registro para determinar si es necesario instalar el paquete de redistribución.                                    |
| [Código de ejemplo para la configuración de redistribución](example-code-for-redistribution-setup.md) | Proporciona código de ejemplo que se puede usar en la rutina de instalación para ejecutar los paquetes de redistribución en modo silencioso y notificar a la rutina de configuración cuando se debe reiniciar el equipo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Consideraciones del proyecto**](project-considerations.md)
</dt> </dl>

 

 




