---
title: StringTable (estructura)
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información de formato de página de códigos y lenguaje para las cadenas especificadas por el miembro Children. Una página de códigos es un juego de caracteres ordenado.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menús de estructura de StringTable y otros recursos
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01ad7a2436c4b32f0f2fa09ab801339903ed55f35be80bbfc43c4542da4e4ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720665"
---
# <a name="stringtable-structure"></a>StringTable (estructura)

Representa la organización de los datos en un recurso de versión de archivo. Contiene información de formato de página de códigos y lenguaje para las cadenas especificadas por el **miembro** Children. Una página de códigos es un juego de caracteres ordenado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, de esta **estructura StringTable,** incluidas todas las estructuras indicadas por el **miembro Children.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Este miembro siempre es igual a cero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo de datos en el recurso de versión. Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Número hexadecimal de 8 dígitos almacenado como una cadena Unicode. Los cuatro dígitos más significativos representan el identificador de idioma. Los cuatro dígitos menos significativos representan la página de códigos para la que se formatearán los datos. Cada identificador de lenguaje estándar de Microsoft contiene dos partes: los 10 bits de orden bajo especifican el idioma principal y los 6 bits de orden superior especifican el sublenguaje. Para obtener una tabla de identificadores válidos, vea .

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tantas palabras cero como sea necesario para alinear el **miembro Children** en un límite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **Cadena**](string-str.md)**

</dd> <dd>

Matriz de una o varias estructuras [**String.**](string-str.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura no es una estructura verdadera del lenguaje C porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos con el Kit de desarrollo de software (SDK) de Windows.

El **miembro Children** de la estructura [**StringFileInfo**](stringfileinfo.md) contiene al menos una **estructura StringTable.**

Establezca la parte de la página de códigos del miembro **szKey** en el valor hexadecimal 0x04b0 para indicar la página de códigos Unicode o en el valor hexadecimal de la página de códigos que sea adecuado para el componente de lenguaje. Después de elegir el valor de la página de códigos, debe seguir usando el mismo valor en revisiones posteriores del archivo.

Un archivo ejecutable o DLL que admita varios idiomas debe tener un recurso de versión para cada lenguaje, en lugar de un único recurso de versión que contenga cadenas en varios idiomas. Sin embargo, si usa la estructura [**Var**](var-str.md) para enumerar los idiomas que admite la aplicación, el número de estructuras **StringTable** del recurso de versión está directamente relacionado con el número de pares de identificadores de página de idioma y de página de códigos en el miembro **Value** de la **estructura Var.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





