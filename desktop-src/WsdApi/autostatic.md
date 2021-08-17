---
description: Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: elemento autoStatic
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f6b9a447e964c90354c909fc0399276d8ed69e7d1dfb3a493d5590a6470d0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738678"
---
# <a name="autostatic-element"></a>elemento autoStatic

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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentarios

El **elemento autoStatic** no es necesario y se puede omitir en el archivo de configuración XML. El elemento se puede usar para deshabilitar la marcación de los campos generados como estáticos o para forzar explícitamente la marcación de determinados campos generados como estáticos.

Los valores posibles son 1 (habilitado, predeterminado) y 0 (deshabilitado). La **habilitación de autoStatic** puede provocar problemas de compilación en función de cómo se dirija el generador de código a los datos de salida.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




