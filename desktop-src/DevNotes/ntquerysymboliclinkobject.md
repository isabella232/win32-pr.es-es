---
description: Recupera el destino de un vínculo simbólico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Función NtQuerySymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 805f3de5da380c4749e58dd7467f1f4ccb2471119ffed81b79695a98feb1b090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003635"
---
# <a name="ntquerysymboliclinkobject-function"></a>Función NtQuerySymbolicLinkObject

\[Esta función puede modificarse o no estar disponible en el futuro.\]

Recupera el destino de un vínculo simbólico.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LinkHandle* \[ En\]
</dt> <dd>

Identificador del objeto de vínculo simbólico.

</dd> <dt>

*LinkTarget* \[ in, out\]
</dt> <dd>

Puntero a una cadena Unicode inicializada que recibe el destino del vínculo simbólico. Los **miembros MaximumLength** y **Buffer** deben establecerse si se produce un error en la llamada.

</dd> <dt>

*ReturnedLength* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe la longitud de la cadena Unicode devuelta en el *parámetro LinkTarget.* Si la función devuelve **STATUS \_ BUFFER TOO \_ \_ SMALL**, esta variable recibe el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **STATUS \_ SUCCESS o** un estado de error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
