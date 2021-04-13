---
title: Grupo de sensores privados
description: Colección de unidades biométricas reservadas para uso exclusivo de una aplicación cliente. Los grupos privados admiten métodos de autenticación propietarios y permiten que una aplicación cliente tenga acceso a una unidad biométrica mediante los comandos de control especificados por el proveedor.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf829290b0e412247b5e629a46e8c0efdafb4880
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269327"
---
# <a name="private-sensor-pool"></a>Grupo de sensores privados

Un grupo de sensores privados es una colección de unidades biométricas reservadas para su uso exclusivo por parte de una aplicación cliente. Los grupos privados admiten métodos de autenticación propietarios y permiten que una aplicación cliente tenga acceso a una unidad biométrica mediante los comandos de control especificados por el proveedor. Unidades biométricas en un grupo de sensores privados:

-   Solo están disponibles para la aplicación cliente que creó el grupo.
-   Enviar avisos de eventos generados por la finalización de las operaciones biométricas directamente a la aplicación sin tener en cuenta el foco de la ventana actual.
-   Use GUID para identificar plantillas biométricas.
-   Compartir una única base de datos de plantilla seleccionada de la aplicación.

Los grupos de sensores privados se deben usar si la aplicación cliente:

-   Administra una colección de unidades biométricas dedicadas que usan una base de datos de plantillas específica de la aplicación. Para ver un ejemplo, considere la posibilidad de usar una aplicación de asistencia de empleados en la que los empleados señalen su llegada en el trabajo deslizando el dedo sobre un lector de huellas digitales. Los empleados no tienen cuentas de Windows en el equipo que ejecuta la aplicación. En su lugar, sus huellas digitales se identifican mediante GUID administrados por la aplicación de asistencia.
-   Recopila muestras biométricas en lugar de simplemente asignar muestras a los SID.
-   Coloca el hardware de la unidad biométrica en modo de mantenimiento para actualizar el firmware.
-   Envía comandos de control definidos por el proveedor al hardware o software de unidad biométrico.
-   Intenta configurar una unidad biométrica con almacenamiento incorporado para que funcione en modo avanzado, pero la unidad no puede realizar las operaciones de hash necesarias.
-   Se ejecuta desde una sesión de cliente de Escritorio remoto.

> [!Note]  
> Las aplicaciones pueden crear grupos de sensores privados únicamente para la biometría de huellas digitales. Si una aplicación intenta crear una para cualquier otra (por ejemplo, una esfera), se producirá un error en la solicitud.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un grupo de sensores privados](creating-a-private-sensor-pool.md)
</dt> <dt>

[Grupos de sensores](sensor-pools.md)
</dt> <dt>

[Grupo de sensores del sistema](system-sensor-pool.md)
</dt> </dl>

 

 




