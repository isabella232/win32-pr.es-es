---
title: StringTable (estructura)
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información sobre el formato del idioma y la página de códigos para las cadenas especificadas por el miembro secundario. Una página de códigos es un juego de caracteres ordenado.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menús de la estructura StringTable y otros recursos
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422054"
---
# <a name="stringtable-structure"></a>StringTable (estructura)

Representa la organización de los datos en un recurso de versión de archivo. Contiene información sobre el formato del idioma y la página de códigos para las cadenas especificadas por el miembro **secundario** . Una página de códigos es un juego de caracteres ordenado.

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

Tipo: **Word**

</dd> <dd>

La longitud, en bytes, de esta estructura **StringTable** , incluidas todas las estructuras indicadas por el miembro **secundario** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Este miembro siempre es igual a cero.

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El tipo de datos del recurso de versión. Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Número hexadecimal de 8 dígitos almacenado como una cadena Unicode. Los cuatro dígitos más significativos representan el identificador de idioma. Los cuatro dígitos menos significativos representan la página de códigos para la que se da formato a los datos. Cada identificador de idioma de Microsoft Standard contiene dos partes: los bits de orden inferior 10 especifican el idioma principal y los 6 bits de orden superior especifican el subidioma. Para obtener una tabla de identificadores válidos, vea.

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **String**](string-str.md)**

</dd> <dd>

Una matriz de una o más estructuras de [**cadena**](string-str.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.

El miembro **secundario** de la estructura [**StringFileInfo**](stringfileinfo.md) contiene al menos una estructura **StringTable** .

Establezca la parte de la página de códigos del miembro **szKey** en el valor hexadecimal 0x04b0 para indicar la página de códigos Unicode o en el valor hexadecimal de la página de códigos que sea adecuado para el componente de lenguaje. Después de elegir el valor de la página de códigos, debe continuar usando el mismo valor en las revisiones posteriores del archivo.

Un archivo ejecutable o DLL que admita varios idiomas debe tener un recurso de versión para cada idioma, en lugar de un único recurso de versión que contenga cadenas en varios idiomas. Sin embargo, si usa la estructura [**var**](var-str.md) para enumerar los idiomas que admite la aplicación, el número de estructuras **StringTable** en el recurso de versión está directamente relacionado con el número de pares de identificador de idioma/página de códigos en el miembro de **valor** de la estructura **var** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**String@**](string-str.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**Distribuidor**](var-str.md)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ versionInfo**](vs-versioninfo.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





