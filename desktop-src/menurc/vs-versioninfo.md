---
title: VS_VERSIONINFO estructura
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
ms.openlocfilehash: 3915cc68ea3207936d8a55c21f4f1e9b0d1d092ec2c4ab80ba210ba6bbc10dd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846925"
---
# <a name="vs_versioninfo-structure"></a>Estructura \_ VERSIONINFO de VS

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

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, de la **estructura \_ VERSIONINFO de VS.** Esta longitud no incluye ningún relleno que alinee los datos de recursos de versión posteriores en un límite de 32 bits.

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, del **miembro Value.** Este valor es cero si no hay ningún **miembro Value** asociado a la estructura de versión actual.

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

Cadena Unicode L"VS \_ VERSION \_ INFO".

</dd> <dt>

**Padding1**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Contiene tantas palabras cero como sea necesario para alinear el **miembro Value** en un límite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**

</dd> <dd>

Datos arbitrarios asociados a esta **estructura \_ VERSIONINFO de VS.** El **miembro wValueLength** especifica la longitud de este miembro; si **wValueLength** es cero, este miembro no existe.

</dd> <dt>

**Padding2**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tantas palabras cero como sea necesario para alinear el **miembro Children** en un límite de 32 bits. Estos bytes no se incluyen en **wValueLength.** Este miembro es opcional.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Matriz de cero o una [**estructura StringFileInfo,**](stringfileinfo.md) y cero o una estructura [**VarFileInfo**](varfileinfo.md) que son elementos secundarios de la estructura **ACTUAL DE VS \_ VERSIONINFO.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura no es una estructura verdadera del lenguaje C porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos con el Kit de desarrollo de software (SDK) de Windows.

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

**Conceptual**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





