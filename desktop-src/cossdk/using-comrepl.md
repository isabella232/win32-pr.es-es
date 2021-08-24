---
description: Uso de COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Uso de COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501cca8d32383e23fc636669e32a80cfdfe96dd658717e41c1618244fc5af81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853885"
---
# <a name="using-comrepl"></a>Uso de COMREPL

Para iniciar la utilidad de línea de comandos COMREPL, siga estos pasos:

1.  Agregue %windir% system32 Com a la ruta de acceso del entorno \\ predeterminada escribiendo lo siguiente en el símbolo del \\ sistema:

    **set path = %PATH%;%windir% \\ system32 \\ Com**

2.  Escriba el siguiente comando COMREPL:

    **COMREPL** *sourceComputer* *targetComputerList* **\[ /n \[ /v \] \]**

    donde:

    -   *sourceComputer es* el nombre del equipo del origen.

    -   *targetComputerList es* los nombres de equipo de los destinos separados por espacios.

    -   **/n suprime** el mensaje de confirmación antes de iniciar la replicación

    -   **/v** hace eco de la salida del archivo de registro en la consola

## <a name="notes"></a>Notas

-   Dado que COM+ no se replica (solo los datos de configuración y las aplicaciones), todos los equipos de destino ya deben tener instalado COM+.
-   El usuario debe pasar comprobaciones de roles para la aplicación del sistema en los equipos de origen y de destino.
-   No se replica ninguna cuenta de máquina local que puedan usar los roles.
-   Los equipos de destino deben estar en línea.
-   El usuario es responsable de replicar todos los datos que no son de COM+ (por ejemplo, tablas de base de datos, archivos de datos, etc.) en los equipos de destino.
-   Los clústeres pueden participar en la replicación, pero tenga en cuenta que COMREPL solo se replica en equipos con nombre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Qué se replica](what-gets-replicated.md)
</dt> </dl>

 

 



