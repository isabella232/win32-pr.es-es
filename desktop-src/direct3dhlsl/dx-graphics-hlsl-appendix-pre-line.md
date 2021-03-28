---
title: " line (Directiva)"
description: Directiva de preprocesador que establece el número de línea y el nombre de archivo almacenados internamente del compilador en los valores especificados.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- HLSL de la Directiva de línea
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419544"
---
# <a name="line-directive"></a>\#line (Directiva)

Directiva de preprocesador que establece el número de línea y el nombre de archivo almacenados internamente del compilador en los valores especificados.



| \#línea *lineNumber* "*nombreDeArchivo*" |
|----------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                              | Descripción                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*<br/>                    | Número de línea que se va a establecer. Puede ser cualquier constante entera. El reemplazo de macros se puede realizar en los tokens de preprocesamiento, siempre que el resultado se evalúe como la sintaxis correcta. <br/>                     |
| <span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nombre de archivo* \[ opta\] <br/> | Nombre de archivo que se va a establecer. El nombre de archivo puede ser cualquier combinación de caracteres y debe incluirse entre comillas dobles (""). Si se omite este parámetro, el nombre de archivo anterior permanece inalterado. <br/> |



 

## <a name="remarks"></a>Observaciones

El compilador usa el número de línea y el nombre de archivo para hacer referencia a los errores que encuentra durante la compilación. El número de línea suele referirse a la línea de entrada actual, y el nombre de archivo hace referencia al archivo de entrada actual. El número de línea se incrementa una vez que se procesa cada línea. Si se cambia el número de línea y el nombre de archivo, el compilador omite los valores anteriores y continúa el procesamiento con los nuevos valores. Los \# generadores de programas suelen usar la directiva line para hacer que los mensajes de error hagan referencia al archivo de código fuente original en lugar de al programa generado.

El traductor usa el número de línea y el nombre de archivo para determinar los valores de la \_ \_ \_ \_ línea y el archivo \_ \_ de \_ macros \_ predefinidos. Estas macros se pueden utilizar para insertar mensajes de error autodescriptivos en el texto del programa. La \_ \_ \_ \_ macro File se expande a una cadena cuyo contenido es el nombre de archivo, entre comillas dobles ("").

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se establece el número de línea en 151 y el nombre de archivo en "Copy. c".


```
#line 151 "copy.c"
```



En el ejemplo siguiente, la macro Assert usa la línea de macros predefinidas \_ \_ \_ \_ y el \_ \_ archivo \_ \_ para imprimir un mensaje de error sobre el archivo de código fuente si la aserción especificada no es true.


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





