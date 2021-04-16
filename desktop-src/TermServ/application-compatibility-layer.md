---
title: Capa de compatibilidad de aplicaciones
description: Para ejecutar aplicaciones heredadas en un entorno de Servicios de Escritorio remoto, puede usar el nivel de compatibilidad de aplicaciones de Servicios de Escritorio remoto.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7bbc5867e42951783d3666aa770cdcc45406f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685786"
---
# <a name="application-compatibility-layer"></a>Capa de compatibilidad de aplicaciones

Para ejecutar aplicaciones heredadas en un entorno de Servicios de Escritorio remoto, puede usar el nivel de compatibilidad de aplicaciones de Servicios de Escritorio remoto. Cuando el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto) carga una aplicación que no es compatible con Servicios de Escritorio remoto, también carga un archivo DLL que contiene el código de compatibilidad. Para usar el nivel de compatibilidad de aplicaciones Servicios de Escritorio remoto, puede establecer la marca NOT TSAWARE al compilar una aplicación.

Si la aplicación es Servicios de Escritorio remoto consciente, puede evitar la sobrecarga de cargar este archivo DLL adicional y ejecutar el código de compatibilidad.

Para indicar que la aplicación es Servicios de Escritorio remoto consciente, establezca la marca de **imagen \_ DLLCHARACTERISTICS \_ \_ \_ compatible con Terminal Server** en el encabezado opcional. Si usa el enlazador que se incluye con Microsoft Visual C++, puede usar la opción del vinculador **TSAWARE** para establecer esta marca. La herramienta **dumpbin** que se incluye con Microsoft Visual C++ proporciona la opción */headers* para determinar el estado de la marca **TSAWARE** . Para obtener más información sobre el uso de la herramienta **dumpbin** , vea [dumpbin Reference](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Tenga cuidado al usar la marca **TSAWARE** porque permite que la aplicación omita cualquier optimización de compatibilidad servicios de escritorio remoto. La marca **TSAWARE** solo debe usarse si está seguro de que la aplicación está diseñada para el entorno de servicios de escritorio remoto. Si la aplicación cumple los siguientes criterios, puede usar de forma segura la marca DLLCHARACTERISTICS de la **imagen \_ \_ compatible con terminal \_ Server \_** .

-   La aplicación no usa archivos. ini.
-   La aplicación no escribe en **HKEY \_ Current \_ User** durante la instalación. Para obtener más información, vea [almacenar información de User-Specific](storing-user-specific-information.md).
-   La aplicación no se ejecuta como un servicio del sistema (es decir, LUID = System).
-   La aplicación no espera acceso exclusivo a las ventanas o a otros directorios del sistema. Esto significa que la aplicación no almacena datos de configuración o temporales por usuario en las ventanas o en otros directorios del sistema.
-   La aplicación no escribe en el subárbol del registro del **equipo local HKEY** para la configuración o los datos específicos del usuario.
-   La aplicación sigue otras instrucciones de compatibilidad Servicios de Escritorio remoto mencionadas en este documento.

 

 