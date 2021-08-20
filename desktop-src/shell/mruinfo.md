---
description: Contiene información que define una nueva lista usada más recientemente (MRU). Lo usa CreateMRUListW.
title: Estructura MRUINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 7f3f18f785bb91a4edcdc3401d595c449cba10b34f155ac71b7c705f2938ea4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049207"
---
# <a name="mruinfo-structure"></a>Estructura MRUINFO

Contiene información que define una nueva lista usada más recientemente (MRU). Utilizado por [**CreateMRUListW.**](createmrulist.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de la estructura.

</dd> <dt>

**Umax**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Número máximo de entradas de la lista de MRU.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Una o varias de las marcas siguientes.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARY** (0x0001)


</dt> <dd>

Los datos se almacenan en el Registro como datos binarios en lugar de datos de cadena.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)


</dt> <dd>

Escriba los cambios en la versión de MRU almacenada en el Registro solo cuando se agrega un nuevo elemento o los recursos de la lista de MRU se liberan de la memoria. Tenga en cuenta que la versión activa de MRU en memoria se actualiza inmediatamente en respuesta a cualquier cambio en el contenido u orden.

</dd> </dl> </dd> <dt>

**hKey**
</dt> <dd>

Tipo: **HKEY**

</dd> <dd>

Identificador de la clave abierta actualmente o uno de los siguientes valores predefinidos en los que almacenar los datos de MRU.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**USUARIO ACTUAL DE HKEY \_ \_**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**HKEY \_ LOCAL \_ MACHINE**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

Tipo: **LPCTSTR**

</dd> <dd>

Subclave en la que se almacenarán los datos de MRU.

</dd> <dt>

**lpfnCompare**
</dt> <dd>

Tipo: **[ **MRUCMPPROC**](mrucmpproc.md)**

</dd> <dd>

Puntero a una función de comparación de datos opcional que se puede usar para determinar si un elemento está presente en la lista de MRU. Esto resulta útil cuando se creó la lista de MRU con la **marca \_ BINARY de MRU.** Si este miembro es **NULL,** se usan funciones de comparación de cadenas estándar; Para los datos binarios, se usa una comparación de memoria directa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura no se define en un archivo de encabezado. Debe definirlo usted mismo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |
| Nombres Unicode y ANSI<br/>   | **MRUINFOW** (Unicode) y **MRUINFOA** (ANSI)<br/>  |



 

 




