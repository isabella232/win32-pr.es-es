---
description: Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: elemento autoStatic
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973706"
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



## <a name="remarks"></a>Observaciones

El **elemento autoStatic** no es necesario y se puede omitir en el archivo de configuración XML. El elemento se puede usar para deshabilitar la marcación de campos generados como estáticos o para forzar explícitamente la marcación de determinados campos generados como estáticos.

Los valores posibles son 1 (habilitado, predeterminado) y 0 (deshabilitado). La **habilitación de autoStatic** puede provocar problemas de compilación en función de cómo se dirija el generador de código a los datos de salida.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




