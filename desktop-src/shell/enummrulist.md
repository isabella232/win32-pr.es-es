---
description: Enumera el contenido de la lista usada más recientemente (MRU). Opcionalmente, recupera un elemento de la enumeración .
title: Función EnumMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 668b92ad8e89c4b3a4082142c7eb8cdc722b8b2f4ce01827319c0480e0d2e997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943005"
---
# <a name="enummrulistw-function"></a>Función EnumMRUListW

\[Esta función está disponible a través Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows. \]

Enumera el contenido de la lista usada más recientemente (MRU). Opcionalmente, recupera un elemento de la enumeración .

## <a name="syntax"></a>Sintaxis


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMRU* \[ En\]
</dt> <dd>

Tipo: **HANDLE**

Identificador de la lista de MRU, obtenido cuando se creó la lista.

</dd> <dt>

*nItem* \[ En\]
</dt> <dd>

Tipo: **int**

Elemento que se devuelve. Si este valor es menor que 0, la función devuelve el número de elementos de la lista de MRU.

</dd> <dt>

*lpData* \[ out\]
</dt> <dd>

Tipo: **\* void**

Puntero a un búfer que recibe el elemento solicitado en *nItem*. Si *nItem* es menor que 0, el contenido de este búfer no cambia.

</dd> <dt>

*uLen* \[ En\]
</dt> <dd>

Tipo: **UINT**

Tamaño del búfer, incluido el carácter nulo de terminación. Si la lista de MRU se creó con la **marca \_ BINARY de MRU,** este es el tamaño en bytes. De lo contrario, es el tamaño en caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve uno de los valores siguientes.

-   Devuelve el número de elementos de la enumeración, si *nItem* es menor que 0.
-   Devuelve -1 si se produjo un error.
-   De lo contrario, devuelve el tamaño de la cadena devuelta *en lpData*, incluido el carácter nulo de terminación. Si la lista de MRU se creó con la **marca \_ BINARY de MRU,** este es el tamaño en bytes. De lo contrario, es el tamaño en caracteres.

## <a name="remarks"></a>Comentarios

Esta función no se incluye en un encabezado o biblioteca públicos. Se puede acceder a él a través de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraerse de comctl32.dll por su ordinal, que es 403 para **EnumMRUListW**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5.0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **EnumMRUListW** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
