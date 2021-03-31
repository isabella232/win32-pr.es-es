---
description: Define el número de la capa de código que se va a generar.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277117"
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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código de WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Los números de capa se utilizan en tablas en tiempo de ejecución para distinguir un nivel de código para otro. WSDAPI utiliza código generado que tiene un número de capa de 0.

Normalmente, este valor será 1, lo que indica que el código generado está en capas en la parte superior de WSDAPI y no en otra capa. En algunos casos, se pueden usar números más altos. Por ejemplo, si una empresa produce código para una clase de dispositivo (capa numerada 1), es posible que un fabricante de hardware determinado desee agregar una capa 2 con número de capa adicional.

Los valores válidos, excepto en el caso del propio WSDAPI, son mayores que 0 y menores que 16.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




