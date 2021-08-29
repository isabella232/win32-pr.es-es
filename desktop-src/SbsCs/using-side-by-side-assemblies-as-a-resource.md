---
description: Usar ensamblados en paralelo como un recurso
ms.assetid: f7963d37-93c4-49d6-af7d-fc692f632894
title: Usar ensamblados en paralelo como un recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eacfffb4c0e8d50db5d00ee514d68191b6550dac0f3df8d69713d5d351a323e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884515"
---
# <a name="using-side-by-side-assemblies-as-a-resource"></a>Usar ensamblados en paralelo como un recurso

Puede agregar un manifiesto a una aplicación como un recurso en el archivo de encabezado ejecutable binario de la aplicación. El valor del identificador de RECURSO DE MANIFIESTO determina cómo usa el cargador las dependencias de ensamblado en paralelo \_ \_ descritas en el manifiesto.

Si establece el identificador de RECURSO DE MANIFIESTO en 1, el cargador usa las dependencias de ensamblado en paralelo especificadas en el manifiesto como valor predeterminado \_ \_ del proceso. Todos los complementos también usan este proceso predeterminado.

En la tabla siguiente se resume cómo el cargador usa el manifiesto para distintos valores de IDENTIFICADOR DE RECURSO DE MANIFIESTO cuando la aplicación se compila con la \_ \_ marca -DISOLATION \_ AWARE \_ ENABLED. Tenga en cuenta que los valores 1-16 están reservados para su uso por Windows XP. Un desarrollador puede usar otros valores si desea administrar los contextos de activación mediante las funciones que se describen en la Referencia de [contexto de activación](activation-context-reference.md).



| Valor de IDENTIFICADOR DE \_ RECURSO DE \_ MANIFIESTO | ¿El manifiesto especifica el valor predeterminado del proceso? | ¿Se usa para las importaciones estáticas? | ¿Se usa para un archivo EXE? | ¿Se usa para un archivo DLL? | ¿Usa la versión en paralelo de los ensamblados si se compila con -DISOLATION \_ AWARE \_ ENABLED? |
|---------------------------------|-----------------------------------------|-------------------------|-----------------|----------------|---------------------------------------------------------------------------------------|
| 1                               | Sí                                     | Sí                     | Sí             | No             | Sí                                                                                   |
| 2                               | No                                      | Sí                     | Sí             | Sí            | Sí                                                                                   |
| 3                               | No                                      | No                      | Sí             | Sí            | Sí                                                                                   |



 

Manifest \_ RESOURCE \_ ID 1 debe usarse para las aplicaciones que no hospedan complementos. Use MANIFEST RESOURCE ID 1 cuando todas las partes de la aplicación deban usar la versión del ensamblado en paralelo \_ \_ especificado en el manifiesto. Para obtener más información, vea [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).

Manifest \_ RESOURCE \_ ID 2 debe usarse para las aplicaciones que hospedan controles o complementos de terceros. En este caso, el manifiesto afecta a todos los ensamblados en paralelo que se cargan mediante carga estática, llamadas a DllMain y llamadas redirigidas por -DISOLATION \_ AWARE \_ ENABLED. Para obtener más información, vea [Enabling an Assembly in an Application Hosting a DLL, Extension, or Panel de control](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

Manifest \_ RESOURCE ID 3 debe usarse para redirigir las llamadas mediante \_ -DISOLATION \_ AWARE ENABLED \_ únicamente. La carga por otros métodos no se ven afectadas.

 

 



