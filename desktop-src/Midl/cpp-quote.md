---
title: cpp_quote (atributo)
description: La \_ palabra clave CPP quote indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote el atributo MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076870"
---
# <a name="cpp_quote-attribute"></a>\_atributo de Comillas CPP

La palabra clave **CPP \_ Quote** indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*string* 
</dt> <dd>

Especifica una cadena entrecomillada que se emite en el archivo de encabezado generado. La cadena debe ir entre comillas para evitar la expansión por parte del preprocesador de C.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El preprocesador del compilador de C procesa las directivas de preprocesamiento de lenguaje c que aparecen en el archivo IDL. Las directivas de **\# definición** en el archivo IDL están disponibles durante la compilación de MIDL pero no están disponibles para el compilador de C.

Por ejemplo, cuando el preprocesador encuentra la Directiva " \# definir Windows 4", el preprocesador reemplaza todas las apariciones de "Windows" en el archivo IDL por "4". El símbolo "WINDOWS" no está disponible durante la compilación en el lenguaje C.

Para permitir que las definiciones de macro del preprocesador de C pasen a través del compilador de MIDL al compilador de C, use la directiva **\# pragma MIDL \_ echo** o **CPP \_ Quote** . Estas directivas indican al compilador de MIDL que genere un archivo de encabezado que contenga la cadena de parámetro con las comillas quitadas. Las directivas **\# pragma MIDL \_ echo** y **CPP \_ Quote** son equivalentes.

El compilador MIDL coloca las cadenas especificadas en las directivas **CPP \_ Quote** y [**pragma**](pragma.md) en el archivo de encabezado en la secuencia en la que se especifican en el archivo IDL y con respecto a otros componentes de la interfaz en el archivo IDL. Las cadenas deben aparecer normalmente en la sección cuerpo de la interfaz de archivo IDL después de todas las operaciones de [**importación**](import.md) .

## <a name="examples"></a>Ejemplos

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importar**](import.md)
</dt> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




