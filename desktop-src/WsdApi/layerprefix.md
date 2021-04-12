---
description: Define el prefijo que se va a usar en el código generado para garantizar la unicidad de los símbolos generados.
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: elemento layerPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b712edee4b33c7158280b9d310624371fd58688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155985"
---
# <a name="layerprefix-element"></a>elemento layerPrefix

Define el prefijo que se va a usar en el código generado para garantizar la unicidad de los símbolos generados.

## <a name="usage"></a>Uso

``` syntax
<layerPrefix/>
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

Cada script del generador de código debe definir una cadena de prefijo única para los módulos creados. Por ejemplo, los scripts de fotogramas de imagen usan un prefijo "PFDEMO".

WSDAPI usa el prefijo "WSD".

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




