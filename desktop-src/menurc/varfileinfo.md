---
title: Estructura VarFileInfo
description: Representa la organización de datos en un recurso de versión de archivo. Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menús de estructura VarFileInfo y otros recursos
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddae8f913e199e0a1219e5ec36012ba3a3eaf24708ca6771ec075b497107418e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733396"
---
# <a name="varfileinfo-structure"></a>Estructura VarFileInfo

Representa la organización de datos en un recurso de versión de archivo. Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.

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

Tipo: **WORD**

</dd> <dd>

Longitud, en bytes, de todo el **bloque VarFileInfo,** incluidas todas las estructuras indicadas por el **miembro** Children.

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

Tipo de datos del recurso de versión. Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Cadena Unicode L"VarFileInfo".

</dd> <dt>

**Relleno**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Tantas palabras cero como sea necesario para alinear el **miembro Children** en un límite de 32 bits.

</dd> <dt>

**Children**
</dt> <dd>

Tipo: **[ **Var**](var-str.md)**

</dd> <dd>

Normalmente contiene una lista de idiomas que admite la aplicación o dll.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no es una estructura verdadera del lenguaje C porque contiene miembros de longitud variable. Esta estructura se creó únicamente para representar la organización de datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos con el Kit de desarrollo de software (SDK) de Windows.

El **miembro Children** de la estructura VS [**\_ VERSIONINFO**](vs-versioninfo.md) puede contener cero o una **estructura VarFileInfo.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**Var**](var-str.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Información de versión](version-information.md)
</dt> </dl>

 

 





