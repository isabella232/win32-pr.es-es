---
description: Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Control de versiones de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8565eb6282fd124c4f43e56d121ba7c053143683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360956"
---
# <a name="tapi-versioning"></a>Control de versiones de TAPI

Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios. Estas nuevas versiones pueden crear nuevas definiciones, como para nuevas características, nuevos miembros en estructuras de datos y nuevos campos de bits. Por lo tanto, los números de versión son necesarios para indicar cómo interpretar varias estructuras de datos.

Para permitir la interoperabilidad óptima de las distintas versiones de aplicaciones, versiones de TAPI propiamente dichas y versiones de proveedores de servicios de diferentes proveedores, la telefonía de Microsoft proporciona un mecanismo de negociación de la versión simple para las aplicaciones. Hay dos versiones diferentes que TAPI y el proveedor de servicios de telefonía deben aceptar para cada dispositivo de línea. La primera es la versión negociada con TAPI y la telefonía básica y complementaria del proveedor de servicios de telefonía (TSP), denominada versión de la interfaz TAPI. El otro es para las extensiones específicas del proveedor, si existen, y se conoce como la versión de la extensión. El formato de las estructuras de datos y los tipos de datos utilizados por las características básicas y complementarias de TAPI se define mediante la versión de TAPI, mientras que la versión de la extensión determina el formato de las estructuras de datos definidas por las extensiones específicas del proveedor.

La función [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) negocia una versión de TAPI y [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negocia la versión de la extensión TSP. Un solo TSP podría ser capaz de administrar más de una versión, y una aplicación debe "revertirse" al uso de una versión anterior si se usa un TSP más antiguo. En **lineNegotiateAPIVersion** , el parámetro *dwApiVersion* tiene como valor predeterminado un valor según la versión, como se indica a continuación.



| Versión de TAPI | Valor predeterminado |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2.0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

No obstante, TAPI facilita esto mucho, siempre que el propio TSP use una versión más reciente que la aplicación. Si el TSP es realmente más reciente, TAPI es capaz de traducir "Down" a la versión de la aplicación. Por ejemplo, TAPI 2,0 profesionales no tienen que ser específicamente capaces de trabajar con la versión 1,4 de TAPI. Si se ejecuta una aplicación TAPI 1,4, TAPI convierte todas las estructuras y mensajes de TAPI 2,0 en equivalentes de TAPI 1,4, o lo más cerca posible. Si no hay ninguna aproximación aproximada en TAPI 1,4, se perderá toda la información específica de TAPI 2,0.

El significado preciso de una versión de extensión es específico del proveedor. Para usar un TSP que admita extensiones, consulte la documentación del proveedor.

Hay varias versiones de TAPI. Aunque la mayoría de estas versiones implican cambios en los conjuntos de documentación de la interfaz del proveedor de servicios de telefonía (TSPI) y TAPI, existen otras implicaciones para cada versión, es decir, diferencias arquitectónicas, variaciones del sistema operativo, redistribuibles y problemas de desarrollo de TSP.



| Versión de TAPI        | Distribución                                                   |
|---------------------|----------------------------------------------------------------|
| 1,0 – 1,2           | Versiones beta que no se deben usar más.              |
| [1.4](tapi-1-4.md) | Incluido en Windows 95.                                        |
| [1.5](tapi-1-5.md) | Incluido en Windows CE 1,0.                                    |
| [2.0](tapi-2-0.md) | Incluido en Windows NT 4,0 con SP3.                           |
| [2.1](tapi-2-1.md) | Incluido en Windows NT 4,0 con SP4 y Windows 98.            |
| [2.2](tapi-2-2.md) | Incluido en Windows Server 2003, Windows XP y Windows 2000. |



 

 

 



