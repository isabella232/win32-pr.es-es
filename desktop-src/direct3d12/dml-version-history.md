---
title: Historial de versiones de DirectML
description: DirectML se distribuye como un componente del sistema de Windows 10 y está disponible como parte del sistema operativo Windows 10 en Windows 10, versión 1903 (10.0; Compilación 18362) y versiones más recientes.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 0a2524faf077b6e4198810395e4aef8da56780af
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282574"
---
# <a name="directml-version-history"></a>Historial de versiones de DirectML

DirectML se distribuye como un componente del sistema de Windows 10 y está disponible como parte del sistema operativo Windows 10 en Windows 10, versión 1903 (10.0; Compilación 18362) y versiones más recientes.

A partir de la versión 1.4.0 de DirectML, DirectML también está disponible como un paquete redistribuible independiente (consulte [Microsoft.AI.DirectML),](https://www.nuget.org/packages/Microsoft.AI.DirectML/)que es útil para las aplicaciones que desean usar una versión fija de DirectML o cuando se ejecutan en versiones anteriores de Windows 10.

DirectML sigue las convenciones [de control de versiones semánticas.](https://semver.org/) Es decir, los números de versión siguen el formato `major.minor.patch` . La primera versión de DirectML tiene una versión de 1.0.0.

## <a name="version-table"></a>Tabla de versiones

|Versión de DirectML|Nivel de característica compatible (consulte Historial [de nivel de características de DirectML)](./dml-feature-level-history.md)|DML_TARGET_VERSION|Primero disponible en|Primero disponible en (Redistributable)|
|-|-|-|-|-|
|1.6.0|DML_FEATURE_LEVEL_4_0|`0x4000`|N/D|[DirectML-1.6.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.6.0)|
|1.5.0|DML_FEATURE_LEVEL_3_1|`0x3100`|N/D|[DirectML-1.5.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.5.0)|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|N/D|[DirectML-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.4.0)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10, versión 2004 (10.0; Compilación 19041) (Windows 10 de mayo de 2020). También conocido como "20H1".|N/D|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10, versión 1903 (10.0; Compilación 18362) (Actualización de mayo de 2019 de Windows 10). También conocido como "19H1".|N/D|

<sup>1</sup> Las versiones intermedias 1.2.0 y 1.3.0 de DirectML no estaban disponibles ampliamente.

## <a name="selecting-a-directml-target-version"></a>Selección de una versión de destino de DirectML

Para mayor comodidad, determinadas características del `DirectML.h` archivo de encabezado se declaran condicionalmente en función del valor de la `DML_TARGET_VERSION` macro. Al establecer la `DML_TARGET_VERSION` macro en determinados valores, puede excluir partes `DirectML.h` de de la aplicación.

Esto puede resultar útil si usa una copia más reciente de , pero tiene como destino una versión inferior del binario de DirectML, ya que garantiza que cualquier intento de usar características más allá del nivel de destino elegido no se `DirectML.h` compilará. Este mecanismo es similar a la `NTDDI_VERSION` macro (vea [Macros para declaraciones condicionales).](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)

Estos son los valores válidos para la `DML_TARGET_VERSION` macro.

|DML_TARGET_VERSION|Efecto|
|-|-|
|`0x4000`|Las características que requieren una versión de DirectML más reciente que **la 1.6.0** se excluyen de `DirectML.h` .|
|`0x3000`|Las características que requieren una versión de DirectML más reciente que **la 1.4.0** se excluyen de `DirectML.h` .|
|`0x2000`|Las características que requieren una versión de DirectML más reciente que **la 1.1.0** se excluyen de `DirectML.h` .|
|`0x1000`|Las características que requieren una versión de DirectML más reciente que **1.0.0** se excluyen de `DirectML.h` .|
|*Sin establecer*|La versión de destino se selecciona automáticamente. Para obtener información más detallada, vea a continuación.|

Si `DML_TARGET_VERSION` no se establece, se selecciona automáticamente mediante lo siguiente.

* Si se `DML_TARGET_VERSION_USE_LATEST` define la macro, se selecciona la versión de destino más reciente.
* De lo contrario, la versión de destino se selecciona en función del valor de la `NTDDI_VERSION` macro.
  *  `NTDDI_WIN10_CO` da como resultado una versión de destino de `0x4000` .
  *  `NTDDI_WIN10_FE` da como resultado una versión de destino de `0x3000` .
  *  `NTDDI_WIN10_VB` da como resultado una versión de destino de `0x2000` .
  *  `NTDDI_WIN10_19H1` da como resultado una versión de destino de `0x1000` .
  *  Si `NTDDI_VERSION` no está definido, se selecciona la versión de destino más reciente (como si `DML_TARGET_VERSION_USE_LATEST` se hubiera especificado).

### <a name="example"></a>Ejemplo

Considere la posibilidad de usar una aplicación con la versión 10.0.19041.0 (Windows 10, versión 2004) del Kit de desarrollo de software (SDK) de Windows. En la tabla anterior, la versión de DirectML a la que se corresponde es 1.1.0 y la correspondiente `DML_TARGET_VERSION` es `0x2000` .

Si no establece ni las macros, la versión de destino seleccionada tendrá como valor predeterminado y todo en estará `DML_TARGET_VERSION` `NTDDI_VERSION` disponible para su `0x2000` `DirectML.h` uso.

Si desea que la aplicación pueda ejecutarse en Windows 10, versión 1903 (10.0; Compilación 18362), podría , lo que excluirá todo el contenido de que no sea compatible con `#define DML_TARGET_VERSION 0x1000` `DirectML.h` DirectML versión 1.0.0. Esto garantiza que cualquier intento de usar la funcionalidad que requiere una versión mayor no se compilará.

## <a name="directml-version-versus-feature-level"></a>Versión de DirectML frente a nivel de característica

La versión de DirectML (por ejemplo, 1.0.0 o 1.4.0) describe una versión determinada de DirectML, incluido su archivo y archivo de encabezado `DirectML.h` `.lib` asociados.

El nivel de característica (por ejemplo, o ) describe la funcionalidad de la implementación subyacente de la API, que puede variar de `DML_FEATURE_LEVEL_1_0` `DML_FEATURE_LEVEL_2_0` la versión de `DirectML.h` utilizada.

Por ejemplo, una aplicación que se compila en un SDK más reciente, pero que se ejecuta en una versión anterior de Windows, podría (en tiempo de ejecución) ver un nivel de características admitido inferior, incluso si se compila con el SDK más reciente.

## <a name="see-also"></a>Vea también

* [Historial de nivel de característica de DirectML](./dml-feature-level-history.md)
* [DML_FEATURE_LEVEL enumeración](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Paquete redistribuible Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)