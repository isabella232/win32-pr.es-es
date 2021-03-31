---
title: Estructura de VS_VERSIONINFO
description: Representa la organización de los datos en un recurso de versión de archivo. Es la estructura raíz que contiene todas las demás estructuras de información de versión de archivo.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO menús de estructura y otros recursos
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151113"
---
# <a name="vs_versioninfo-structure"></a>Estructura de VS \_ versionInfo

Representa la organización de los datos en un recurso de versión de archivo. Es la estructura raíz que contiene todas las demás estructuras de información de versión de archivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

La longitud, en bytes, de la estructura de **vs \_ versionInfo** . Esta longitud no incluye ningún relleno que alinee los datos de recursos de versiones posteriores en un límite de 32 bits.

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

La longitud, en bytes, del miembro de **valor** . Este valor es cero si no hay ningún miembro de **valor** asociado a la estructura de la versión actual.

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

Cadena Unicode L "información de \_ versión de vs \_ ".

</dd> <dt>

**Padding1**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Contiene tantas palabras cero como sea necesario para alinear el miembro de **valor** en un límite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**

</dd> <dd>

Datos arbitrarios asociados con esta estructura de **vs \_ versionInfo** . El miembro **wValueLength** especifica la longitud de este miembro; Si **wValueLength** es cero, este miembro no existe.

</dd> <dt>

**Padding2**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits. Estos bytes no se incluyen en **wValueLength**. Este miembro es opcional.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Una matriz de cero o una estructura [**StringFileInfo**](stringfileinfo.md) , y una o ninguna de las estructuras [**VarFileInfo**](varfileinfo.md) que son elementos secundarios de la estructura actual de **vs \_ versionInfo** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[**VarFileInfo**](varfileinfo.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

**Vista**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





