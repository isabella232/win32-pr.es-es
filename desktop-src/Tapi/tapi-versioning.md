---
description: Obtenga información sobre el control de versiones de TAPI. Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Control de versiones de TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f940cead427f843bb7cf3a3a89e1747344a8ffa2ddb8fff5a2b30db0b5a7f2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872895"
---
# <a name="tapi-versioning"></a>Control de versiones de TAPI

Con el tiempo, se pueden generar diferentes versiones de TAPI, aplicaciones y proveedores de servicios. Estas nuevas versiones pueden crear nuevas definiciones, como para nuevas características, nuevos miembros en estructuras de datos y nuevos campos de bits. Por lo tanto, los números de versión son necesarios para indicar cómo interpretar varias estructuras de datos.

Para permitir una interoperabilidad óptima de diferentes versiones de aplicaciones, versiones del propio TAPI y versiones de proveedores de servicios de distintos proveedores, Microsoft Telefonía proporciona un mecanismo de negociación de versiones simple para las aplicaciones. Hay dos versiones diferentes en las que TAPI y el proveedor de servicios de telefonía deben ponerse de acuerdo para cada dispositivo de línea. La primera es la versión negociada con TAPI y la telefonía básica y complementaria del proveedor de servicios de telefonía (TSP), lo que se conoce como la versión de la interfaz TAPI. La otra es para extensiones específicas del proveedor, si las hay, y se conoce como la versión de la extensión. El formato de las estructuras de datos y los tipos de datos utilizados por las características Básica y Complementaria de TAPI se define mediante la versión de TAPI, mientras que la versión de la extensión determina el formato de las estructuras de datos definidas por las extensiones específicas del proveedor.

La [**función lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) negocia una versión tapi y [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negocia la versión de la extensión TSP. Un único TSP podría ser capaz de controlar más de una versión y una aplicación debe "volver atrás" al uso de una versión anterior si se usa un TSP anterior. En **lineNegotiateAPIVersion, el** parámetro *dwApiVersion* tiene como valor predeterminado un valor según la versión, como se muestra a continuación.



| Versión de TAPI | Valor predeterminado |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2.0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

Sin embargo, TAPI facilita esto siempre que el propio TSP use una versión más reciente que la aplicación. Si el TSP es realmente más reciente, TAPI es capaz de traducir "hacia abajo" a la versión de la aplicación. Por ejemplo, los TSP de TAPI 2.0 no necesitan ser específicamente capaces de trabajar con TAPI versión 1.4. Si se ejecuta una aplicación TAPI 1.4, TAPI convierte todas las estructuras y mensajes de TAPI 2.0 en equivalentes de TAPI 1.4 o lo más cerca posible. Si no hay ninguna aproximación cercana en TAPI 1.4, se perderá toda la información específica de TAPI 2.0.

El significado preciso de una versión de extensión es específico del proveedor. Para usar un TSP que admita extensiones, consulte la documentación del proveedor.

Hay varias versiones de TAPI. Aunque la mayoría de estas versiones implicaban cambios en los conjuntos de documentación tapi y de interfaz de proveedor de servicios de telefonía (TSPI), hay otras implicaciones para cada versión, es decir, las diferencias de arquitectura, las variaciones del sistema operativo, los redistribuibles y los problemas de desarrollo de TSP.



| Versión de TAPI        | Distribución                                                   |
|---------------------|----------------------------------------------------------------|
| 1.0 – 1.2           | Versiones beta que ya no se deben usar.              |
| [1.4](tapi-1-4.md) | Se incluye en Windows 95.                                        |
| [1.5](tapi-1-5.md) | Incluido en Windows CE 1.0.                                    |
| [2.0](tapi-2-0.md) | Se incluye Windows NT 4.0 con SP3.                           |
| [2.1](tapi-2-1.md) | Se incluye Windows NT 4.0 con SP4 y Windows 98.            |
| [2.2](tapi-2-2.md) | Se incluye en Windows Server 2003, Windows XP y Windows 2000. |



 

 

 



