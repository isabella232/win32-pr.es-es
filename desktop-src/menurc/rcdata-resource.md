---
title: Recurso RCDATA
description: Define un recurso de datos sin procesar para una aplicación. Los recursos de datos sin procesar permiten la inclusión de datos binarios directamente en el archivo ejecutable.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menús de recursos RCDATA y otros recursos
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f813bde1195d8adcad708c40857cc11b1e7b70f696455168e174a4bf2f6cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847045"
---
# <a name="rcdata-resource"></a>Recurso RCDATA

Define un recurso de datos sin procesar para una aplicación. Los recursos de datos sin procesar permiten la inclusión de datos binarios directamente en el archivo ejecutable.

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Este parámetro puede ser cero o más de las siguientes instrucciones.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**CHARACTERISTICS**](characteristics-statement.md). |
| [**Language**](language-statement.md) *Language*, *sublanguage* | Idioma del recurso. Para obtener más información, vea [**LANGUAGE**](language-statement.md).                                                                                            |
| [**VERSION**](version-statement.md) *dword*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*datos sin procesar*
</dt> <dd>

Datos sin procesar que constan de uno o varios enteros o cadenas de caracteres. Los enteros se pueden especificar en formato decimal, octal o hexadecimal. Para que sean compatibles con los valores de 16 Windows bits, los enteros se almacenan como **valores WORD.** Puede almacenar un entero como un **valor DWORD** si califica el entero con el sufijo "L".

Las cadenas se incluyen entre comillas. RC no anexa automáticamente un carácter nulo de terminación a una cadena. Cada cadena es una secuencia de los caracteres ANSI especificados, a menos que la califique como una cadena de caracteres anchos con el prefijo L.

El bloque de datos comienza en un **límite DWORD** y RC no realiza ningún relleno ni alineación de los datos dentro del *bloque de datos sin* procesar. Es su responsabilidad garantizar la alineación adecuada de los datos dentro del bloque.

</dd> </dl>

Algunos atributos también se admiten para la compatibilidad con versiones anteriores. Para obtener más información, vea [Atributos de recursos comunes](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción RCDATA:**

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Lengua**](language-statement.md)
</dt> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 




