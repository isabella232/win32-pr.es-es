---
description: Usar COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Usar COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807628"
---
# <a name="using-comrepl"></a>Usar COMREPL

Para iniciar la utilidad de línea de comandos COMREPL, siga estos pasos:

1.  Agregue% WINDIR% \\ system32 \\ com a la ruta de acceso predeterminada del entorno; para ello, escriba lo siguiente en el símbolo del sistema:

    **establecer ruta de acceso =% PATH%;% WINDIR% \\ system32 \\ com**

2.  Escriba el siguiente comando de COMREPL:

    **COMREPL** *es sourcecomputer,* *targetComputerList* **\[ \[ /n \] /v \]**

    donde:

    -   *es sourcecomputer,* es el nombre de equipo del origen.

    -   *targetComputerList* son los nombres de equipo de los destinos separados por espacios

    -   **/n** suprime la solicitud de confirmación antes de iniciar la replicación

    -   **/v** muestra la salida del archivo de registro en la consola

## <a name="notes"></a>Notas

-   Dado que no se replica COM+ (solo los datos y las aplicaciones de configuración), todos los equipos de destino deben tener instalado COM+.
-   El usuario debe pasar las comprobaciones de roles para la aplicación del sistema en los equipos de origen y de destino.
-   No se replican las cuentas de equipo local que puedan usar los roles.
-   Los equipos de destino deben estar en línea.
-   El usuario es responsable de replicar todos los datos que no son COM (por ejemplo, tablas de base de datos, archivos de datos, etc.) en los equipos de destino.
-   Los clústeres pueden participar en la replicación, pero tenga en cuenta que COMREPL solo se replica en equipos con nombre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Lo que se replica](what-gets-replicated.md)
</dt> </dl>

 

 



