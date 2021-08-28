---
title: Capa de compatibilidad de aplicaciones
description: Para ejecutar aplicaciones heredadas en un entorno Servicios de Escritorio remoto, puede usar el Servicios de Escritorio remoto compatibilidad de aplicaciones.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3630346578801e4d2578db6f528048914412dc9ad1a8544e2c2d303188814b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099615"
---
# <a name="application-compatibility-layer"></a>Capa de compatibilidad de aplicaciones

Para ejecutar aplicaciones heredadas en un entorno Servicios de Escritorio remoto, puede usar el Servicios de Escritorio remoto compatibilidad de aplicaciones. Cuando el Escritorio remoto host de sesión de escritorio remoto carga una aplicación que no es compatible Servicios de Escritorio remoto, también carga un archivo DLL que contiene código de compatibilidad. Para usar la Servicios de Escritorio remoto compatibilidad de aplicaciones, puede establecer la marca NOT TSAWARE al compilar una aplicación.

Si la aplicación es Servicios de Escritorio remoto, puede evitar la sobrecarga de cargar este archivo DLL adicional y ejecutar el código de compatibilidad.

Para indicar que la aplicación es Servicios de Escritorio remoto, establezca la marca **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER \_ \_ AWARE** en el encabezado opcional. Si usa el vinculador que se incluye con Microsoft Visual C++, puede usar la opción del vinculador **TSAWARE** para establecer esta marca. La **herramienta DUMPBIN** que se incluye con Microsoft Visual C++ proporciona la opción */HEADERS* para determinar el estado de la **marca TSAWARE.** Para obtener más información sobre el uso de **la herramienta DUMPBIN,** vea [Referencia de DUMPBIN](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Tenga cuidado al usar la marca **TSAWARE** porque permite que la aplicación omita cualquier optimización Servicios de Escritorio remoto compatibilidad. La **marca TSAWARE solo** debe usarse si está seguro de que la aplicación está diseñada para el entorno Servicios de Escritorio remoto cliente. Si la aplicación cumple los siguientes criterios, puede usar de forma segura la marca **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER \_ \_ AWARE.**

-   La aplicación no usa .ini archivos.
-   La aplicación no escribe en **HKEY \_ CURRENT USER \_ durante** la instalación. Para obtener más información, vea [Almacenar User-Specific información.](storing-user-specific-information.md)
-   La aplicación no se ejecuta como un servicio del sistema (es decir, LUID=System).
-   La aplicación no espera acceso exclusivo a la Windows directorios del sistema. Esto significa que la aplicación no almacena datos temporales o de configuración por usuario en el Windows o en otros directorios del sistema.
-   La aplicación no escribe en el subárbol del Registro **de HKEY Local Machine** para los datos o la configuración específicos del usuario.
-   La aplicación sigue otras Servicios de Escritorio remoto de compatibilidad mencionadas en este documento.

 

 