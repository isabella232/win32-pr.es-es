---
description: Define el prefijo que se va a utilizar en el código generado para los nombres de macros en el espacio de nombres.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715801"
---
# <a name="macroprefix-element"></a>elemento macroPrefix

Define el prefijo que se va a utilizar en el código generado para los nombres de macros en el espacio de nombres.

## <a name="usage"></a>Uso

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                   | Descripción                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**System.IO**](namespace.md)<br/> | Espacio de nombres que se va a utilizar para la generación de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este elemento invalida el prefijo de URI predeterminado utilizado para las macros generadas. Por ejemplo, si el prefijo de la macro es "AV \_ " y el nombre es "sintonizador", la macro generada para el nombre completo será " \_ sintonizador de AV".

De forma predeterminada, el código generado crea un prefijo de macro preferido a partir del URI.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




