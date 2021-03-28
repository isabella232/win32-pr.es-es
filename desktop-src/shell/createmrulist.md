---
description: Crea una nueva lista de elementos usados más recientemente (MRU).
title: CreateMRUListW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808834"
---
# <a name="createmrulistw-function"></a>CreateMRUListW función)

Crea una nueva lista de elementos usados más recientemente (MRU).

## <a name="syntax"></a>Sintaxis


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LPMI* \[ de\]
</dt> <dd>

Tipo: **LPMRUINFO**

Puntero a una estructura [**MRUINFO**](mruinfo.md) que define la lista MRU.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve un identificador para la nueva lista MRU o 0 en caso de error.

## <a name="remarks"></a>Observaciones

Esta función no está incluida en un encabezado público o una biblioteca. Se puede tener acceso a ella a través de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraer de comctl32.dll por su ordinal, que es 400 para **CreateMRUListW**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5,0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CreateMRUListW** (Unicode)<br/>                                                                        |



 

 
