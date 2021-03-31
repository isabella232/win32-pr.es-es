---
description: Usar ensamblados en paralelo como un recurso
ms.assetid: f7963d37-93c4-49d6-af7d-fc692f632894
title: Usar ensamblados en paralelo como un recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b97265b48f4ce8f3c87a87ec4ca9ea2b8252819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001058"
---
# <a name="using-side-by-side-assemblies-as-a-resource"></a>Usar ensamblados en paralelo como un recurso

Puede Agregar un manifiesto a una aplicación como un recurso en el archivo de encabezado ejecutable binario de la aplicación. El valor del identificador de \_ recurso de manifiesto \_ determina cómo el cargador usa las dependencias de ensamblado en paralelo descritas en el manifiesto.

Si establece el identificador de \_ recurso de manifiesto \_ en 1, el cargador usa las dependencias de ensamblado en paralelo especificadas en el manifiesto como el valor predeterminado del proceso. Todos los complementos también usan este proceso predeterminado.

En la tabla siguiente se resume cómo el cargador usa el manifiesto para los distintos valores del identificador de recurso del manifiesto \_ \_ cuando la aplicación se compila con la marca-DISOLATION \_ compatible con \_ . Tenga en cuenta que los valores 1-16 están reservados para su uso en Windows XP. Un desarrollador puede usar otros valores si desea administrar los contextos de activación mediante las funciones descritas en la [referencia de contexto de activación](activation-context-reference.md).



| Valor del \_ identificador de recurso del manifiesto \_ | El manifiesto especifica el valor predeterminado del proceso? | ¿Usar para las importaciones estáticas? | ¿Usar para un archivo EXE? | ¿Usar para un archivo DLL? | ¿Usa la versión en paralelo de los ensamblados si están compilados con el reconocimiento de DISOLATION \_ \_ habilitado? |
|---------------------------------|-----------------------------------------|-------------------------|-----------------|----------------|---------------------------------------------------------------------------------------|
| 1                               | Sí                                     | Sí                     | Sí             | No             | Sí                                                                                   |
| 2                               | No                                      | Sí                     | Sí             | Sí            | Sí                                                                                   |
| 3                               | No                                      | No                      | Sí             | Sí            | Sí                                                                                   |



 

El \_ \_ identificador de recurso 1 del manifiesto se debe usar para las aplicaciones que no hospedan complementos. Use \_ el identificador de recurso de manifiesto \_ 1 cuando todas las partes de la aplicación deben usar la versión del ensamblado en paralelo especificada en el manifiesto. Para obtener más información, vea [habilitar un ensamblado en una aplicación sin extensiones](enabling-an-assembly-in-an-application-without-extensions.md).

El \_ \_ identificador de recurso 2 del manifiesto debe usarse para las aplicaciones que hospedan controles o complementos de terceros. En este caso, el manifiesto afecta a todos los ensamblados en paralelo que se cargan mediante carga estática, llamadas a DllMain y llamadas redirigidas por-DISOLATION \_ \_ habilitada. Para obtener más información, vea [habilitar un ensamblado en una aplicación que hospeda un archivo dll, una extensión o un panel de control](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

\_El ID. de recurso \_ de manifiesto 3 debe usarse para redirigir llamadas solo con el reconocimiento de DISOLATION \_ \_ habilitado. La carga de otros métodos no se ve afectada.

 

 



