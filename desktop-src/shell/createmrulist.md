---
description: Crea una nueva lista usada más recientemente (MRU).
title: Función CreateMRUListW
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
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468273"
---
# <a name="createmrulistw-function"></a>Función CreateMRUListW

Crea una nueva lista usada más recientemente (MRU).

## <a name="syntax"></a>Sintaxis


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpmi* \[ En\]
</dt> <dd>

Tipo: **LPMRUINFO**

Puntero a una estructura [**MRUINFO que**](mruinfo.md) define la lista de MRU.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve un identificador a la nueva lista de MRU o 0 en caso de error.

## <a name="remarks"></a>Observaciones

Esta función no se incluye en un encabezado o biblioteca públicos. Se puede acceder a él a través de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraerse de comctl32.dll por su ordinal, que es 400 para **CreateMRUListW**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5.0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CreateMRUListW** (Unicode)<br/>                                                                        |



 

 
