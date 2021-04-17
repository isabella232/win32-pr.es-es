---
title: Estructura VarFileInfo
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menús de la estructura VarFileInfo y otros recursos
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714609"
---
# <a name="varfileinfo-structure"></a>Estructura VarFileInfo

Representa la organización de los datos en un recurso de versión de archivo. Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

La longitud, en bytes, del bloque **VarFileInfo** completo, incluidas todas las estructuras indicadas por el miembro **secundario** .

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

Cadena Unicode L "VarFileInfo".

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **var**](var-str.md)**

</dd> <dd>

Normalmente contiene una lista de idiomas compatibles con la aplicación o el archivo DLL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.

El miembro **secundario** de la estructura de [**vs \_ versionInfo**](vs-versioninfo.md) puede contener cero o una estructura **VarFileInfo** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**Distribuidor**](var-str.md)
</dt> <dt>

[**VS \_ versionInfo**](vs-versioninfo.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





