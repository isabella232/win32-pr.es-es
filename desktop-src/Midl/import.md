---
title: import (atributo)
description: La directiva import especifica otro archivo IDL, ODL o de encabezado que contiene las definiciones a las que desea hacer referencia desde el archivo IDL principal.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- ATRIBUTO DE IMPORTACIÓN MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd389d56dff242132c628beedaf9c70d697f1fead0286aa0b59cd492a5a1e882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040091"
---
# <a name="import-attribute"></a>import (atributo)

La **directiva import** especifica otro archivo IDL, ODL o de encabezado que contiene las definiciones a las que desea hacer referencia desde el archivo IDL principal.

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*filename* 
</dt> <dd>

Especifica el nombre del archivo de encabezado, IDL o ODL que se importará.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Con la **directiva import,** todas las instrucciones IDL del archivo importado, como typedefs, declaraciones constantes y definiciones de interfaz, están disponibles para la importación. Archivo IDL.

El archivo importado se procesa por separado (lo que significa que el preprocesador CPP se invoca de forma independiente) del archivo IDL de importación. De esta manera, las directivas de preprocesador, como define, no se llevan de un encabezado importado o un archivo IDL al archivo \# IDL de importación.

Al igual que la macro de preprocesador del lenguaje C, incluye , la directiva **import** indica al compilador que incluya los tipos de datos definidos en los archivos IDL importados. **\#** A diferencia **\# de la directiva include,** la directiva **import** omite los prototipos de procedimiento, ya que no se genera código auxiliar para nada en el archivo importado.

Para obtener información específica sobre el uso **de import** para incluir archivos de encabezado en un archivo IDL, vea [Importing System Header Files](importing-system-header-files.md).

Encabezado de lenguaje C (. El archivo H) generado para la interfaz no contiene directamente los tipos importados, sino que genera una directiva **\# include** para el archivo de encabezado correspondiente a la interfaz importada. Por ejemplo, al importar BASE. IDL en EL DERIVADO. IDL, el archivo de encabezado generado DERIVADO. H contendrá la directiva **\# include** BASE.H.

Se aplican las reglas siguientes:

-   La **palabra clave import** es opcional y puede aparecer cero o más veces en el archivo IDL.
-   Cada **palabra clave** import se puede asociar a más de un nombre de archivo.
-   Separe varios nombres de archivo con comas.
-   Debe incluir el nombre de archivo entre comillas y finalizar la instrucción de importación con un punto y coma (;).
-   Puede importar una interfaz que no tenga atributos en otro archivo IDL. Sin embargo, la interfaz solo debe contener tipos de datos; no puede contener ningún procedimiento. Si incluso hay un procedimiento contenido en la interfaz importada, debe especificar un atributo [**UUID**](uuid.md) [**o local.**](local.md)
-   La **función** de importación es idempotente, es decir, la importación de una interfaz más de una vez no tiene ningún efecto adicional.

> [!Note]  
> El comportamiento de la **directiva de** importación es independiente de los modificadores de modo del compilador MIDL [**/ms \_ ext**](-ms-ext.md) (valor predeterminado), [**/osf**](-osf.md)y [**/app \_ config**](-app-config.md). Sin embargo, el modo del compilador (**/osf** o **/ms \_ ext**) puede afectar a la decoración de atributos de puntero en los tipos importados. Para obtener más información, [vea Herencia de tipos de atributo de puntero.](/windows/desktop/Rpc/pointer-attribute-type-inheritance)

 

## <a name="examples"></a>Ejemplos

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**incluír**](include.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 