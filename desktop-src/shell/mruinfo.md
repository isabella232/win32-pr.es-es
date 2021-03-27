---
description: Contiene información que define una nueva lista de elementos usados más recientemente (MRU). Usado por CreateMRUListW.
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
ms.openlocfilehash: 91c0b1a2c10f4ac77afa5f8af2380b3d14ced8f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997261"
---
# <a name="mruinfo-structure"></a>Estructura MRUINFO

Contiene información que define una nueva lista de elementos usados más recientemente (MRU). Usado por [**CreateMRUListW**](createmrulist.md).

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

**Escáner**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Número máximo de entradas en la lista MRU.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Una o varias de las marcas siguientes.

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARIo** (0x0001)


</dt> <dd>

Los datos se almacenan en el registro como datos binarios en lugar de datos de cadena.

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)


</dt> <dd>

Escriba los cambios en la versión de MRU almacenada en el registro solo cuando se agregue un nuevo elemento o se liberen los recursos de la lista MRU de la memoria. Tenga en cuenta que la versión activa de las MRU en memoria se actualiza inmediatamente en respuesta a cualquier cambio en el contenido o la ordenación.

</dd> </dl> </dd> <dt>

**hKey**
</dt> <dd>

Tipo: **HKEY**

</dd> <dd>

Identificador de la clave abierta actualmente o uno de los siguientes valores predefinidos en los que se van a almacenar los datos de la MRU.

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

**HKEY \_ Current \_ User**
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

**HKEY \_ local \_ Machine**
</dt> </dl> </dd> <dt>

**lpszSubKey**
</dt> <dd>

Tipo: **LPCTSTR**

</dd> <dd>

Subclave en la que se almacenan los datos de MRU.

</dd> <dt>

**lpfnCompare**
</dt> <dd>

Tipo: **[ **MRUCMPPROC**](mrucmpproc.md)**

</dd> <dd>

Puntero a una función de comparación de datos opcional que se puede usar para determinar si un elemento está presente en la lista MRU. Esto resulta útil cuando la lista MRU se creó con la **marca \_ binaria MRU** . Si este miembro es **null**, se usan las funciones de comparación de cadenas estándar; en el caso de los datos binarios, se usa una comparación de memoria directa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no está definida en un archivo de encabezado. Debe definirlo por sí mismo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |
| Nombres Unicode y ANSI<br/>   | **MRUINFOW** (Unicode) y **MRUINFOA** (ANSI)<br/>  |



 

 




