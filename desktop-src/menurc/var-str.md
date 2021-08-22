---
title: Estructura var
description: Representa la organización de datos en un recurso de versión de archivo. Normalmente contiene una lista de pares de idioma y identificador de página de códigos que admite la versión de la aplicación o dll.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menús de estructura var y otros recursos
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48537009b56d2b37f4508871049463a65a12965c31658e932716832955503f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599585"
---
# <a name="var-structure"></a>Estructura var

Representa la organización de datos en un recurso de versión de archivo. Normalmente contiene una lista de pares de idioma y identificador de página de códigos que admite la versión de la aplicación o dll.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, de la **estructura Var.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, del **miembro Value.**

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tipo de datos del recurso de versión. Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Cadena Unicode L"Translation".

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tantas palabras cero como sea necesario para alinear el **miembro Value** en un límite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Matriz de uno o varios valores que son pares de identificadores de página de códigos y lenguaje. Para obtener más información, vea la sección Comentarios siguiente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura no es una estructura verdadera del lenguaje C porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos con el Kit de desarrollo de software (SDK) de Windows.

Si usa la estructura **Var** para enumerar los idiomas que admite la aplicación o dll en lugar de usar varios recursos de versión, use el miembro **Value** para contener una matriz de valores **DWORD** que indique las combinaciones de idioma y página de códigos admitidas por este archivo. La palabra de orden bajo de cada **DWORD** debe contener un identificador de idioma de Microsoft y la palabra de orden superior debe contener el número de página de códigos de IBM. La palabra de orden alto o bajo puede ser cero, lo que indica que el archivo es independiente del idioma o de la página de códigos. Si se omite la estructura **Var,** el archivo se interpretará como independiente del lenguaje y de la página de códigos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





