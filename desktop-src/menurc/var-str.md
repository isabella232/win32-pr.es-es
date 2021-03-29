---
title: Estructura var
description: Representa la organización de los datos en un recurso de versión de archivo. Normalmente contiene una lista de los pares de idioma y de identificador de página de códigos que admite la versión de la aplicación o DLL.
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
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905607"
---
# <a name="var-structure"></a>Estructura var

Representa la organización de los datos en un recurso de versión de archivo. Normalmente contiene una lista de los pares de idioma y de identificador de página de códigos que admite la versión de la aplicación o DLL.

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

Tipo: **Word**

</dd> <dd>

Longitud, en bytes, de la estructura **var** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

La longitud, en bytes, del miembro de **valor** .

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

Cadena Unicode L "Translation".

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palabras como sea necesario para alinear el miembro de **valor** en un límite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Matriz de uno o más valores que son pares de identificador de idioma y página de códigos. Para obtener más información, vea la sección Comentarios siguiente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.

Si usa la estructura **var** para enumerar los idiomas admitidos por la aplicación o el archivo dll en lugar de usar varios recursos de versión, use el miembro de **valor** para contener una matriz de valores **DWORD** que indiquen las combinaciones de idioma y página de códigos admitidas por este archivo. La palabra de orden inferior de cada **DWORD** debe contener un identificador de idioma de Microsoft y la palabra de orden superior debe contener el número de página de códigos de IBM. La palabra de orden superior o de orden inferior puede ser cero, lo que indica que el archivo es independiente del idioma o de la página de códigos. Si se omite la estructura **var** , el archivo se interpretará como independiente del lenguaje y de la página de códigos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**VS \_ versionInfo**](vs-versioninfo.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





