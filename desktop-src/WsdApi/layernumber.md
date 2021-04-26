---
description: Define el número de la capa de código que se va a generar.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995492"
---
# <a name="layernumber-element"></a>elemento layerNumber

Define el número de la capa de código que se va a generar.

## <a name="usage"></a>Uso

``` syntax
<layerNumber/>
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

Los números de capa se usan en tablas en tiempo de ejecución para distinguir una capa de código para otra. El propio WSDAPI usa código generado que tiene un número de capa de 0.

Normalmente, este valor será 1, lo que indica que el código generado está en capas sobre WSDAPI y ninguna otra capa. En algunos casos, se pueden usar números más altos. Por ejemplo, si una empresa genera código para una clase de dispositivo (nivel numerado 1), es posible que un proveedor de hardware determinado quiera agregar una capa adicional numerada de capa 2.

Los valores legales, excepto en el caso del propio WSDAPI, son mayores que 0 y menores que 16.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




