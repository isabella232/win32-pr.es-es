---
description: Enumera el contenido de la lista de elementos usados más recientemente (MRU). Opcionalmente, recupera un elemento de la enumeración.
title: EnumMRUListW función)
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
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912366"
---
# <a name="enummrulistw-function"></a>EnumMRUListW función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows. \]

Enumera el contenido de la lista de elementos usados más recientemente (MRU). Opcionalmente, recupera un elemento de la enumeración.

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

*hMRU* \[ de\]
</dt> <dd>

Tipo: **Handle**

Identificador de la lista MRU, obtenida cuando se creó la lista.

</dd> <dt>

*nItem* \[ de\]
</dt> <dd>

Tipo: **int**

Elemento que se va a devolver. Si este valor es menor que 0, la función devuelve el número de elementos de la lista MRU.

</dd> <dt>

*lpData* \[ enuncia\]
</dt> <dd>

Tipo: **void \** _

Un puntero a un búfer que recibe el elemento solicitado en _nItem *. Si *nItem* es menor que 0, el contenido de este búfer no cambia.

</dd> <dt>

*uLen* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del búfer, incluido el carácter nulo de terminación. Si la lista MRU se creó con la **marca \_ binaria MRU** , este es el tamaño en bytes. De lo contrario, es el tamaño en caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Devuelve uno de los valores siguientes.

-   Devuelve el número de elementos de la enumeración, si *nItem* es menor que 0.
-   Devuelve-1 si se ha producido un error.
-   De lo contrario, devuelve el tamaño de la cadena devuelta en *lpData*, incluido el carácter nulo de terminación. Si la lista MRU se creó con la **marca \_ binaria MRU** , este es el tamaño en bytes. De lo contrario, es el tamaño en caracteres.

## <a name="remarks"></a>Observaciones

Esta función no está incluida en un encabezado público o una biblioteca. Se puede tener acceso a ella a través de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraer de comctl32.dll por su ordinal, que es 403 para **EnumMRUListW**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5,0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **EnumMRUListW** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
