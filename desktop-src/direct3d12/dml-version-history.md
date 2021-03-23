---
title: Historial de versiones de DirectML
description: DirectML se distribuye como un componente del sistema de Windows 10 y está disponible como parte del sistema operativo Windows 10 (SO) en Windows 10, versión 1903 (10,0; Compilación 18362) y versiones más recientes.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 04cb7a2c906d7674c793a9a99e21609ea874dbc1
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104549197"
---
# <a name="directml-version-history"></a>Historial de versiones de DirectML

DirectML se distribuye como un componente del sistema de Windows 10 y está disponible como parte del sistema operativo Windows 10 (SO) en Windows 10, versión 1903 (10,0; Compilación 18362) y versiones más recientes.

A partir de la versión de DirectML 1.4.0, DirectML también está disponible como paquete redistribuible independiente (vea [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)), que es útil para las aplicaciones que quieren usar una versión fija de DirectML o cuando se ejecutan en versiones anteriores de Windows 10.

DirectML sigue las convenciones [semánticas de control de versiones](https://semver.org/) . Es decir, los números de versión siguen el formulario `major.minor.patch` . La primera versión de DirectML tiene una versión de 1.0.0.

## <a name="version-table"></a>Tabla de versiones

|Versión de DirectML|Nivel de característica compatible (vea el [historial de nivel de características de DirectML](./dml-feature-level-history.md))|DML_TARGET_VERSION|Primera disponible en|Primer disponible en (redistribuible)|
|-|-|-|-|-|-|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|N/D|[DirectML-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10, versión 2004 (10,0; Compilación 19041) (actualización de Windows 10 mayo de 2020). También conocido como "20H1".|N/D|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10, versión 1903 (10,0; Compilación 18362) (actualización de Windows 10 mayo de 2019). También conocido como "19H1".|N/D|

<sup>1</sup> las versiones intermedias de 1.3.0 y 1.2.0 de DirectML no estaban disponibles de forma generalizada.

## <a name="selecting-a-directml-target-version"></a>Selección de una versión de destino de DirectML

Para mayor comodidad, algunas características del `DirectML.h` archivo de encabezado se declaran condicionalmente según el valor de la `DML_TARGET_VERSION` macro. Al establecer la `DML_TARGET_VERSION` macro en determinados valores, puede excluir partes de `DirectML.h` la aplicación.

Esto puede ser útil si está utilizando una copia más reciente de `DirectML.h` , pero tiene como destino una versión inferior del archivo binario DirectML, porque garantiza que cualquier intento de usar características más allá del nivel de destino elegido no se compilará. Este mecanismo es similar a la `NTDDI_VERSION` macro (vea [macros para declaraciones condicionales](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)).

Estos son los valores válidos de la `DML_TARGET_VERSION` macro.

|DML_TARGET_VERSION|Efecto|
|-|-|
|`0x3000`|Todas las características que requieren una versión de DirectML más reciente que **1.4.0** se excluyen de `DirectML.h` .|
|`0x2000`|Todas las características que requieren una versión de DirectML más reciente que **1.1.0** se excluyen de `DirectML.h` .|
|`0x1000`|Todas las características que requieren una versión de DirectML más reciente que **1.0.0** se excluyen de `DirectML.h` .|
|*Sin establecer*|La versión de destino se selecciona automáticamente. Para obtener información más detallada, vea a continuación.|

Si `DML_TARGET_VERSION` no se establece, se selecciona automáticamente de la siguiente manera.

* Si `DML_TARGET_VERSION_USE_LATEST` se define la macro, se selecciona la última versión de destino.
* De lo contrario, la versión de destino se selecciona en función del valor de la `NTDDI_VERSION` macro.
  *  `NTDDI_WIN10_19H1` da como resultado una versión de destino de `0x1000` .
  *  `NTDDI_WIN10_VB` da como resultado una versión de destino de `0x2000` .
  *  Si `NTDDI_VERSION` no se define, se selecciona la última versión de destino (como si `DML_TARGET_VERSION_USE_LATEST` se especificara).

### <a name="example"></a>Ejemplo

Considere una aplicación que usa la versión 10.0.19041.0 (Windows 10, versión 2004) del kit de desarrollo de software (SDK) de Windows. En la tabla anterior, la versión de DirectML que corresponde a es 1.1.0 y el correspondiente `DML_TARGET_VERSION` es `0x2000` .

Si no establece `DML_TARGET_VERSION` ni las `NTDDI_VERSION` macros, la versión de destino seleccionada se establecerá de forma predeterminada en `0x2000` y estará `DirectML.h` disponible para su uso.

Si desea que la aplicación se pueda ejecutar en Windows 10, versión 1903 (10,0; Compilación 18362), puede `#define DML_TARGET_VERSION 0x1000` , que excluirá todo el contenido de `DirectML.h` que no sea compatible con la versión 1.0.0 de DirectML. Esto garantiza que cualquier intento de usar una funcionalidad que requiera una versión mayor no se compilará.

## <a name="directml-version-versus-feature-level"></a>Versión de DirectML frente a nivel de característica

La versión de DirectML (por ejemplo, 1.0.0 o 1.4.0) describe una versión determinada de DirectML, incluido el archivo `DirectML.h` de encabezado y el `.lib` archivo asociados.

El nivel de característica (por ejemplo, `DML_FEATURE_LEVEL_1_0` o `DML_FEATURE_LEVEL_2_0` ) describe la capacidad de la implementación subyacente de la API, que puede variar de la versión de `DirectML.h` utilizada.

Por ejemplo, una aplicación que se compila con un SDK más reciente, pero que se ejecuta en una versión anterior de Windows, podría (en tiempo de ejecución) ver un nivel de característica compatible inferior, incluso si se compila con el SDK más reciente.

## <a name="see-also"></a>Consulte también

Historial de nivel de [característica de DirectML](./dml-feature-level-history.md) 
 [Enumeración DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [Paquete redistribuible de Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)