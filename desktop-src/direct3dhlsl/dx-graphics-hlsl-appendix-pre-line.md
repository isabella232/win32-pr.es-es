---
title: " line (Directiva)"
description: Directiva de preprocesador que establece el número de línea y el nombre de archivo almacenados internamente del compilador en los valores especificados.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- line (Directiva HLSL)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568393"
---
# <a name="line-directive"></a>\#line (Directiva)

Directiva de preprocesador que establece el número de línea y el nombre de archivo almacenados internamente del compilador en los valores especificados.



| \#line *lineNumber* "*filename*" |
|----------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                              | Descripción                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*<br/>                    | Número de línea que se establece. Puede ser cualquier constante de entero. El reemplazo de macro se puede realizar en los tokens de preprocesamiento, siempre que el resultado se evalúe como la sintaxis correcta. <br/>                     |
| <span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[ Opcional\] <br/> | Nombre de archivo que se establecerá. El nombre de archivo puede ser cualquier combinación de caracteres y debe ir entre comillas dobles (" "). Si se omite este parámetro, el nombre de archivo anterior permanece sin cambios. <br/> |



 

## <a name="remarks"></a>Observaciones

El compilador usa el número de línea y el nombre de archivo para hacer referencia a los errores que encuentra durante la compilación. El número de línea suele referirse a la línea de entrada actual, y el nombre de archivo hace referencia al archivo de entrada actual. El número de línea se incrementa una vez que se procesa cada línea. Si se cambia el número de línea y el nombre de archivo, el compilador omite los valores anteriores y continúa el procesamiento con los nuevos valores. Los generadores de programas suelen usar la directiva de línea para que los mensajes de error haga referencia al archivo de código fuente original en \# lugar de al programa generado.

El traductor usa el número de línea y el nombre de archivo para determinar los valores de las macros \_ \_ predefinidas FILE \_ \_ y LINE \_ \_ \_ \_ . Estas macros se pueden utilizar para insertar mensajes de error autodescriptivos en el texto del programa. La \_ \_ macro FILE se \_ \_ expande a una cadena cuyo contenido es el nombre de archivo, entre comillas dobles (" ").

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se establece el número de línea en 151 y el nombre de archivo en "copy.c".


```
#line 151 "copy.c"
```



En el ejemplo siguiente, la macro ASSERT usa las macros predefinidas LINE y FILE para imprimir un mensaje de error sobre el archivo de origen si la aserción especificada \_ \_ \_ \_ no \_ \_ es \_ \_ verdadera.


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





