---
title: Cadenas de formato
description: Una cadena de formato es un token interpretado que el motor NDR entiende. Las cadenas de formato se conocen a menudo como MOPs; en esta documentación se usa la cadena de formato de término en todo.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563dd9e4145a7d83b2e49f180329c05c1d55155d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776963"
---
# <a name="format-strings"></a>Cadenas de formato

Una cadena de formato es un token interpretado que el motor NDR entiende. Las cadenas de formato se conocen a menudo como MOPs; en esta documentación se usa la cadena de formato de término en todo.

Para ser más precisos, un carácter de formato es un token interpretable individual (atómico). Cada carácter de formato tiene un byte de tamaño. Una cadena de formato es una secuencia de caracteres de formato o caracteres de formato y datos numéricos. El descriptor de términos también se utiliza para asignar nombres a las secuencias comunes. por ejemplo, una cadena de formato de parámetro o un descriptor de parámetro es una cadena de formato que se usa para describir un parámetro de una rutina.

Los caracteres de formato tienen nombres simbólicos propuestos, como FC \_ Long o FC \_ struct. Todos los caracteres de cadena de formato usados por MIDL y el motor NDR se definen en el archivo Ndrtypes. h.

## <a name="format-string-tables"></a>Tablas de cadenas de formato

El motor utiliza dos tablas de cadenas de formato principal: la tabla de cadenas de formato de procedimiento, **\_ \_ MIDL \_ ProcFormatString**, que mantiene los descriptores de procedimiento y la tabla de cadenas de formato de tipo, **\_ \_ MIDL \_ TypeFormatString**, que mantiene los descriptores de tipo de datos. El compilador genera ambos en los archivos de código auxiliar principales ( \* \_ c. c, \* \_ s. c, \* \_ p. c). La tabla de cadenas de formato de procedimiento la usan principalmente varios intérpretes, pero también se usa para la conversión de búfer, independientemente del modo del compilador. La tabla de cadenas de formato de tipo se usa al llamar al motor de NDR principal para indicar los tipos de datos específicos en los que se va a trabajar.

## <a name="format-string-notation"></a>Notación de cadena de formato

La notación usada en este documento sigue las instrucciones de descripción de programación comunes, con una barra ( \| ) que se usa para indicar construcciones alternativas y corchetes ( \[ \] ) que se usan para indicar elementos opcionales. Las cadenas de formato suelen apilarse para mejorar la legibilidad (responsabilidad). En todo este documento, FC denota un solo carácter de formato. Los caracteres de formato se presentan en MAYÚSCULAs, con sus nombres simbólicos reales. Otros campos arbitrarios se representan mediante un nombre y un tamaño.

Los corchetes angulares ( <> ) se utilizan para indicar los tamaños de los descriptores. Se emplean las convenciones que se muestran en la tabla siguiente.



| Notación     | Significado                                                   |
|--------------|-----------------------------------------------------------|
| <*n*>  | El tamaño del descriptor es n bytes.                        |
| <>     | El tamaño del descriptor varía.                            |
| {<>}\* | El descriptor se repite un número de veces (0, 1, 2...). |



 

Los siguientes caracteres de formato tienen un significado especial.



| Carácter | Significado                                   |
|-----------|-------------------------------------------|
| final de FC \_   | Indica el final de algunas cadenas de formato. |
| Pad de FC \_   | Carácter controlador no interpretado.              |



 

 

 




