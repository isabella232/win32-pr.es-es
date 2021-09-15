---
title: StringFileInfo (estructura)
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información de versión que se puede mostrar para un idioma y una página de códigos determinados.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menús de estructura StringFileInfo y otros recursos
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468546"
---
# <a name="stringfileinfo-structure"></a>StringFileInfo (estructura)

Representa la organización de los datos en un recurso de versión de archivo. Contiene información de versión que se puede mostrar para un idioma y una página de códigos determinados.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a>Members

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, de todo el **bloque StringFileInfo,** incluidas todas las estructuras indicadas por el **miembro** Children.

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

Cadena Unicode L"StringFileInfo".

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tantas palabras cero como sea necesario para alinear el **miembro Children** en un límite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **StringTable**](stringtable.md)**

</dd> <dd>

Matriz de una o varias estructuras [**StringTable.**](stringtable.md) El miembro **szKey** de cada estructura **StringTable** indica el idioma y la página de códigos adecuados para mostrar el texto en esa **estructura StringTable.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura verdadera del lenguaje C porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos con el Kit de desarrollo de software (SDK) de Windows.

El **miembro Children** de la estructura VS [**\_ VERSIONINFO**](vs-versioninfo.md) puede contener cero o más **estructuras StringFileInfo.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**String**](string-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





