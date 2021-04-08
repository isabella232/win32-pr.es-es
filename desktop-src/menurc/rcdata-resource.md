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
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994762"
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

Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*
</dt> <dd>

Este parámetro puede ser cero o más de las instrucciones siguientes.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* del idioma, *subidioma* | Idioma del recurso. Para obtener más información, vea [**Language**](language-statement.md).                                                                                            |
| [**Versión**](version-statement.md) *DWORD*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**versión**](version-statement.md).              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*datos sin procesar*
</dt> <dd>

Datos sin procesar que se componen de uno o varios enteros o cadenas de caracteres. Los enteros se pueden especificar en formato decimal, octal o hexadecimal. Para ser compatible con Windows de 16 bits, los enteros se almacenan como valores de **Word** . Puede almacenar un entero como valor **DWORD** si califica el entero con el sufijo "L".

Las cadenas se incluyen entre comillas. RC no anexa automáticamente un carácter nulo de terminación a una cadena. Cada cadena es una secuencia de los caracteres ANSI especificados, a menos que la califique como una cadena de caracteres anchos con el prefijo L.

El bloque de datos comienza en un límite **DWORD** y RC no realiza ningún relleno ni alineación de los datos en el bloque de *datos sin procesar* . Es su responsabilidad garantizar la correcta alineación de los datos dentro del bloque.

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso de la instrucción **RCDATA** :

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

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 




