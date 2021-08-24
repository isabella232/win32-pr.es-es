---
title: Recurso STRINGTABLE
description: Define uno o varios recursos de cadena para una aplicación. Los recursos de cadena son simplemente cadenas Unicode o ASCII terminadas en NULL que se pueden cargar cuando sea necesario desde el archivo ejecutable mediante la función LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menús de recursos STRINGTABLE y otros recursos
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7994b6853195ba164c766ca6ee275e4535ab1249c0c78907ab996b9dc644013a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720655"
---
# <a name="stringtable-resource"></a>Recurso STRINGTABLE

Define uno o varios recursos de cadena para una aplicación. Los recursos de cadena son simplemente cadenas Unicode o ASCII terminadas en NULL que se pueden cargar cuando sea necesario desde el archivo ejecutable mediante la [**función LoadString.**](/windows/win32/api/winuser/nf-winuser-loadstringa)

Hay dos maneras de dar formato a **una instrucción STRINGTABLE:**

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- O bien

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*
</dt> <dd>

Este parámetro puede ser cero o más de las instrucciones siguientes.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**CHARACTERISTICS**](characteristics-statement.md). |
| [**Language**](language-statement.md) *language*, *sublanguage* | Especifica el idioma del recurso. Para obtener más información, vea [**LANGUAGE**](language-statement.md).                                                                              |
| [**VERSION**](version-statement.md) *dword*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**VERSION**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

Entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*Cadena*
</dt> <dd>

Una o varias cadenas, entre comillas. La cadena no debe tener más de 4097 caracteres y debe ocupar una sola línea en el archivo de origen. Para agregar un retorno de carro a la cadena, use esta secuencia de caracteres: \\ 012. Por ejemplo, "Línea \\ uno 012Line dos" define una cadena que se muestra de la siguiente manera:

``` syntax
Line one
Line two
```

Para insertar comillas en la cadena, use la siguiente secuencia: "". Por ejemplo, """Línea tres""" define una cadena que se muestra de la siguiente manera:

``` syntax
"Line three"
```

Para codificar caracteres Unicode, use una "L" seguida de los caracteres Unicode entre comillas. Consulte la sección Ejemplos para obtener un ejemplo.

El compilador de recursos también admite continuaciones de línea en *la cadena*. Consulte la sección Ejemplos para obtener un ejemplo.

</dd> </dl>

Algunos atributos también se admiten por compatibilidad con versiones anteriores. Para más información, consulte [Atributos de recursos comunes.](common-resource-attributes.md)

## <a name="remarks"></a>Comentarios

RC asigna 16 cadenas por sección y usa el valor de identificador para determinar qué sección debe contener la cadena. Las cadenas cuyos identificadores difieren solo en los 4 bits inferiores se colocan en la misma sección. Para obtener más información, [vea Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción STRINGTABLE** para mostrar cadenas ASCII:

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

En el ejemplo siguiente se muestra cómo codificar caracteres Unicode:

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

En el ejemplo siguiente se muestran cadenas con ASCII y Unicode. Tenga en cuenta que las cadenas sin la "L" inicial usan el formato de escape de 2 dígitos:

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

En el ejemplo siguiente se muestra cómo se pueden usar las continuaciones de línea:

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Lengua**](language-statement.md)
</dt> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 