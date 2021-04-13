---
title: import (atributo)
description: La Directiva Import especifica otro archivo IDL, ODL o de encabezado que contiene las definiciones a las que desea hacer referencia desde el archivo IDL principal.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- importar el atributo MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358851"
---
# <a name="import-attribute"></a>import (atributo)

La directiva **Import** especifica otro archivo IDL, ODL o de encabezado que contiene las definiciones a las que desea hacer referencia desde el archivo IDL principal.

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*filename* 
</dt> <dd>

Especifica el nombre del archivo de encabezado, IDL o ODL que se va a importar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Con la Directiva de **importación** , todas las instrucciones idl del archivo importado, como definiciones de tipo, declaraciones de constantes y definiciones de interfaz, pasan a estar disponibles para la importación. Archivo IDL.

El archivo importado se procesa por separado (lo que significa que el preprocesador CPP se invoca de forma independiente) desde el archivo IDL de importación. De esta manera, las directivas de preprocesador, como \# definir, no se exportan desde un archivo IDL o de encabezado importado al archivo IDL de importación.

Como la macro de preprocesador de lenguaje C **\# incluye**, la directiva **Import** indica al compilador que incluya los tipos de datos que se definieron en los archivos IDL importados. A diferencia de la directiva **\# include** , la directiva **Import** omite los prototipos de procedimiento, ya que no se genera ningún código auxiliar para nada en el archivo importado.

Para obtener información específica sobre cómo usar **importar** para incluir archivos de encabezado en un archivo IDL, vea [importar archivos de encabezado del sistema](importing-system-header-files.md).

Encabezado del lenguaje C (. H) generado para la interfaz no contiene directamente los tipos importados, sino que genera una directiva **\# include** para el archivo de encabezado correspondiente a la interfaz importada. Por ejemplo, al importar BASE. IDL en el derivado. IDL, derivado del archivo de encabezado generado. H contendrá la directiva **\# include** base. H.

Se aplican las reglas siguientes:

-   La palabra clave **Import** es opcional y puede aparecer cero o más veces en el archivo IDL.
-   Cada palabra clave de **importación** puede asociarse a más de un nombre de archivo.
-   Separe varios nombres de archivo con comas.
-   Debe escribir el nombre de archivo entre comillas y finalizar la instrucción de importación con un punto y coma (;).
-   Puede importar una interfaz que no tenga atributos en otro archivo IDL. Sin embargo, la interfaz debe contener solo tipos de contenido; no puede contener ningún procedimiento. Si hay un procedimiento incluido en la interfaz importada, debe especificar un atributo [**local**](local.md) o [**UUID**](uuid.md) .
-   La función de **importación** es idempotentÂ â € "â es decir, la importación de una interfaz más de una vez no tiene ningún efecto adicional.

> [!Note]  
> El comportamiento de la Directiva de **importación** es independiente del modo de compilador de MIDL modificadores [**/MS \_ ext**](-ms-ext.md) (el valor predeterminado), [**/OSF**](-osf.md)y [**/App \_ config**](-app-config.md). Sin embargo, el modo de compilador (**/OSF** o **/MS \_ ext**) puede afectar a la decoración de atributos de puntero en los tipos importados. Para obtener más información, vea [herencia de tipos de atributos de puntero](/windows/desktop/Rpc/pointer-attribute-type-inheritance).

 

## <a name="examples"></a>Ejemplos

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**configuración de/APP \_**](-app-config.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**inclui**](include.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[**\_ext/MS**](-ms-ext.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 