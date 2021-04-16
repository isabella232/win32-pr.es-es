---
description: Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: Autostatic (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715813"
---
# <a name="autostatic-element"></a>Autostatic (elemento)

Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos. Este comportamiento está habilitado de forma predeterminada.

## <a name="usage"></a>Uso

``` syntax
<autoStatic/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código de WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

El elemento **Autostatic** no es necesario y se puede omitir en el archivo de configuración XML. El elemento se puede utilizar para deshabilitar la marca de los campos generados como estáticos o para forzar explícitamente la marca de determinados campos generados como estáticos.

Los valores posibles son 1 (habilitado, predeterminado) y 0 (deshabilitado). La habilitación de **Autostatic** puede producir problemas de compilación en función de cómo se dirija el generador de código a los datos de salida.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




