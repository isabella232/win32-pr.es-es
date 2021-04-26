---
description: Define el prefijo que se usará en el código generado para garantizar la unidad de los símbolos generados.
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: elemento layerPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98970013c72600affd7d4d9e7a71781f477cd87d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994702"
---
# <a name="layerprefix-element"></a>elemento layerPrefix

Define el prefijo que se usará en el código generado para garantizar la unidad de los símbolos generados.

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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Cada script generador de código debe definir una cadena de prefijo única para los módulos creados. Por ejemplo, los scripts de fotogramas de imagen usan un prefijo de "PFDEMO".

WSDAPI usa el prefijo "WSD".

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




