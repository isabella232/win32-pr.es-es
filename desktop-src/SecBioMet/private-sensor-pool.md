---
title: Grupo de sensores privado
description: Colección de unidades biométricas reservadas para uso exclusivo por una aplicación cliente. Los grupos privados admiten métodos de autenticación propietarios y permiten que una aplicación cliente acceda a una unidad biométrica mediante comandos de control especificados por el proveedor.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf829290b0e412247b5e629a46e8c0efdafb4880
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271348"
---
# <a name="private-sensor-pool"></a>Grupo de sensores privado

Un grupo de sensores privado es una colección de unidades biométricas reservadas para uso exclusivo por una aplicación cliente. Los grupos privados admiten métodos de autenticación propietarios y permiten que una aplicación cliente acceda a una unidad biométrica mediante comandos de control especificados por el proveedor. Unidades biométricas en un grupo de sensores privado:

-   Solo están disponibles para la aplicación cliente que creó el grupo.
-   Envíe los avisos de eventos generados por la finalización de operaciones biométricas directamente a la aplicación sin tener en cuenta el foco de ventana actual.
-   Use GUID para identificar plantillas biométricas.
-   Comparta una base de datos de plantilla única seleccionada por la aplicación.

Los grupos de sensores privados deben usarse si la aplicación cliente:

-   Administra una colección de unidades biométricas dedicadas que usan una base de datos de plantilla específica de la aplicación. Por ejemplo, considere una aplicación de asistencia a empleados en la que los empleados señalen su llegada al trabajo deslizando el dedo en un lector de huellas digitales. Los empleados no tienen Windows en el equipo que ejecuta la aplicación. En su lugar, sus huellas digitales se identifican mediante GUID administrados por la aplicación de asistencia.
-   Recopila muestras biométricas en lugar de simplemente asigna muestras a SID.
-   Coloca el hardware de la unidad biométrica en modo de mantenimiento para actualizar el firmware.
-   Envía comandos de control definidos por el proveedor al hardware o software de la unidad biométrica.
-   Intenta configurar una unidad biométrica con almacenamiento incorporado para que funcione en modo avanzado, pero la unidad no puede realizar las operaciones de hash necesarias.
-   Se ejecuta desde una Escritorio remoto cliente.

> [!Note]  
> Las aplicaciones pueden crear grupos de sensores privados solo para biometría de huellas digitales. Si una aplicación intenta crear una para cualquier otra cosa (por ejemplo, Face), se producirá un error en la solicitud.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un grupo de sensores privado](creating-a-private-sensor-pool.md)
</dt> <dt>

[Grupos de sensores](sensor-pools.md)
</dt> <dt>

[Grupo de sensores del sistema](system-sensor-pool.md)
</dt> </dl>

 

 




