---
title: Recurso STRINGTABLE
description: Define uno o más recursos de cadena para una aplicación. Los recursos de cadena son simplemente cadenas Unicode o ASCII terminadas en null que se pueden cargar cuando es necesario desde el archivo ejecutable, mediante la función LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menús de recursos de STRINGTABLE y otros recursos
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149267"
---
# <a name="stringtable-resource"></a>Recurso STRINGTABLE

Define uno o más recursos de cadena para una aplicación. Los recursos de cadena son simplemente cadenas Unicode o ASCII terminadas en null que se pueden cargar cuando es necesario desde el archivo ejecutable, mediante la función [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .

Hay dos maneras de dar formato a una instrucción **stringtable** :

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

\- o -

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

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*
</dt> <dd>

Este parámetro puede ser cero o más de las instrucciones siguientes.



| .                                                        | Descripción                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* del idioma, *subidioma* | Especifica el idioma del recurso. Para obtener más información, vea [**Language**](language-statement.md).                                                                              |
| [**Versión**](version-statement.md) *DWORD*                     | Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos. Para obtener más información, vea [**versión**](version-statement.md).              |



 

</dd> <dt>

<span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*
</dt> <dd>

Entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="string"></span><span id="STRING"></span>*String@*
</dt> <dd>

Una o más cadenas, entre comillas. La cadena no debe tener más de 4097 caracteres y debe ocupar una sola línea en el archivo de código fuente. Para agregar un retorno de carro a la cadena, use esta secuencia de caracteres: \\ 012. Por ejemplo, "line One \\ 012Line two" define una cadena que se muestra de la siguiente manera:

``` syntax
Line one
Line two
```

Para insertar comillas en la cadena, use la siguiente secuencia: "". Por ejemplo, "" "línea tres" "" define una cadena que se muestra de la siguiente manera:

``` syntax
"Line three"
```

Para codificar caracteres Unicode, utilice una "L" seguida de los caracteres Unicode entre comillas. Vea la sección ejemplos para obtener un ejemplo.

El compilador de recursos también admite continuaciones de línea en la *cadena*. Vea la sección ejemplos para obtener un ejemplo.

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="remarks"></a>Observaciones

RC asigna 16 cadenas por sección y usa el valor del identificador para determinar qué sección va a contener la cadena. Las cadenas cuyos identificadores difieren solo en los 4 bits inferiores se colocan en la misma sección. Para obtener más información, vea [Q196774](https://support.microsoft.com/kb/196774).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la instrucción **stringtable** para mostrar cadenas ASCII:

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

[**Fall**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 