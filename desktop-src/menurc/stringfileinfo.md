---
title: Estructura StringFileInfo
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información de versión que se puede mostrar para un idioma y una página de códigos determinados.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menús de la estructura StringFileInfo y otros recursos
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996065"
---
# <a name="stringfileinfo-structure"></a>Estructura StringFileInfo

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



## <a name="members"></a>Miembros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

La longitud, en bytes, del bloque **StringFileInfo** completo, incluidas todas las estructuras indicadas por el miembro **secundario** .

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

Cadena Unicode L "StringFileInfo".

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **StringTable**](stringtable.md)**

</dd> <dd>

Una matriz de una o más estructuras de [**StringTable**](stringtable.md) . Cada miembro **szKey** de la estructura **stringtable** indica el idioma y la página de códigos adecuados para mostrar el texto en esa estructura de **stringtable** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.

El miembro **secundario** de la estructura de [**vs \_ versionInfo**](vs-versioninfo.md) puede contener cero o más estructuras **StringFileInfo** .

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

[**String@**](string-str.md)
</dt> <dt>

[**VS \_ versionInfo**](vs-versioninfo.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





