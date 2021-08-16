---
description: Cierra un identificador de búsqueda.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose (función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 862159ed74d6c7c9ddbe4d6f97bede37bab7dca949e6d3259715737de07b8df5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758725"
---
# <a name="cscfindclose-function"></a>CSCFindClose (función)

\[Esta función no se admite y no se debe usar.\]

Cierra un identificador de búsqueda.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFind* \[ En\]
</dt> <dd>

Identificador de búsqueda devuelto por la [**función CSCFindFirstFileW.**](cscfindfirstfilew.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSCFindFirstFileW**](cscfindfirstfilew.md)
</dt> </dl>

 

 
