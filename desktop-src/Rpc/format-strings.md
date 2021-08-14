---
title: Cadenas de formato
description: Una cadena de formato es un token interpretado que el motor de BAND entiende. Las cadenas de formato se conocen a menudo como MOP; en esta documentación se usa el término cadena de formato en todo.
ms.assetid: 548283bd-023a-41dd-b1d0-661305d019e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8c14fa649e71411c5706193e83fd9a09d30f8a0c57fec411d8c34fef675ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929872"
---
# <a name="format-strings"></a>Cadenas de formato

Una cadena de formato es un token interpretado que el motor de BAND entiende. Las cadenas de formato se conocen a menudo como MOP; en esta documentación se usa el término cadena de formato en todo.

Para ser más precisos, un carácter de formato es un token individual (atómico) interpretable. Cada carácter de formato tiene un byte de tamaño. Una cadena de formato es una secuencia de caracteres de formato o caracteres de formato y datos numéricos. El descriptor de término también se usa para asignar nombres a secuencias comunes; Por ejemplo, una cadena de formato de parámetro o un descriptor de parámetros es una cadena de formato que se usa para describir un parámetro de una rutina.

Los caracteres de formato tienen nombres simbólicos sugerentes como FC \_ LONG o FC \_ STRUCT. Todos los caracteres de cadena de formato usados por MIDL y el motor BYTE se definen en el archivo Types.h.

## <a name="format-string-tables"></a>Dar formato a tablas de cadenas

El motor usa dos tablas de cadenas de formato principal: la tabla de cadenas de formato de procedimiento, **\_ \_ MIDL \_ ProcFormatString**, que mantiene los descriptores de procedimiento; y la tabla de cadenas de formato de tipo, **\_ \_ MIDL \_ TypeFormatString**, que mantiene los descriptores de tipos de datos. El compilador genera ambos en los archivos de código auxiliar principales \* \_ (c.c, \* \_ s.c, \* \_ p.c). La tabla de cadenas de formato de procedimiento la usan principalmente varios intérpretes, pero también se usa para la conversión del búfer independientemente del modo del compilador. La tabla de cadenas de formato de tipo se usa al llamar al motor JPEG principal para indicar los tipos de datos específicos en los que se va a trabajar.

## <a name="format-string-notation"></a>Formato de la notación de cadena

La notación usada en este documento sigue las instrucciones de descripción de programación comunes, con una barra ( ) que se usa para denotar construcciones alternativas y corchetes ( ) que se usan para indicar elementos \| \[ \] opcionales. Las cadenas de formato se apilan con frecuencia para mejorar la legibilidad (responsabilidad). A lo largo de este documento, FC denota un carácter de formato único. Los caracteres de formato se presentan en todos los CAPS, con sus nombres simbólicos reales. Otros campos arbitrarios se representan mediante un nombre y un tamaño.

Los corchetes angulares ( <> ) se usan para indicar los tamaños de los descriptores. Se emplean las convenciones que se muestran en la tabla siguiente.



| Notación     | Significado                                                   |
|--------------|-----------------------------------------------------------|
| <*N*>  | El tamaño del descriptor es de n bytes.                        |
| <>     | El tamaño del descriptor varía.                            |
| {<>}\* | El descriptor se repite varias veces (0,1,2 ...). |



 

Los siguientes caracteres de formato tienen un significado especial.



| Carácter | Significado                                   |
|-----------|-------------------------------------------|
| FC \_ END   | Indica el final de algunas cadenas de formato. |
| FC \_ PAD   | Carácter de panel sin interpretar.              |



 

 

 




