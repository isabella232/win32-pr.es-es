---
title: cpp_quote (atributo)
description: La palabra clave cpp quote indica a MIDL que emita la cadena especificada, sin los caracteres de \_ comillas, en el archivo de encabezado generado.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote atributo MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159643"
---
# <a name="cpp_quote-attribute"></a>cpp \_ quote attribute

La **palabra clave cpp \_ quote** indica a MIDL que emita la cadena especificada, sin los caracteres de comillas, en el archivo de encabezado generado.

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*string* 
</dt> <dd>

Especifica una cadena entre comillas que se emite en el archivo de encabezado generado. La cadena debe estar entrecomillada para evitar la expansión por parte del preprocesador de C.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El preprocesador del compilador de C procesa las directivas de preprocesamiento del lenguaje C que aparecen en el archivo IDL. Las **\# directivas define** del archivo IDL están disponibles durante la compilación MIDL, pero no están disponibles para el compilador de C.

Por ejemplo, cuando el preprocesador encuentra la directiva "define WINDOWS 4", el preprocesador reemplaza todas las apariciones de "WINDOWS" en el archivo \# IDL por "4". El símbolo "WINDOWS" no está disponible durante la compilación del lenguaje C.

Para permitir que las definiciones de macro del preprocesador de C pasen a través del compilador MIDL al compilador de C, use la directiva **\# pragma midl \_ echo** o **cpp \_ quote.** Estas directivas indica al compilador MIDL que genere un archivo de encabezado que contenga la cadena de parámetro con las comillas quitadas. Las **\# directivas pragma midl \_ echo** y **cpp \_ quote** son equivalentes.

El compilador MIDL coloca las cadenas especificadas en las directivas **cpp \_ quote** y [**pragma**](pragma.md) en el archivo de encabezado en la secuencia en la que se especifican en el archivo IDL y en relación con otros componentes de interfaz del archivo IDL. Las cadenas deberían aparecer normalmente en la sección cuerpo de la interfaz de archivo IDL después de todas las [**operaciones de**](import.md) importación.

## <a name="examples"></a>Ejemplos

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Importación**](import.md)
</dt> <dt>

[**Pragma**](pragma.md)
</dt> </dl>

 

 




