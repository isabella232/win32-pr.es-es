---
description: Recupera el destino de un vínculo simbólico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject función)
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
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649628"
---
# <a name="ntquerysymboliclinkobject-function"></a>NtQuerySymbolicLinkObject función)

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

*LinkHandle* \[ de\]
</dt> <dd>

Identificador del objeto de vínculo simbólico.

</dd> <dt>

*LinkTarget* \[ in, out\]
</dt> <dd>

Puntero a una cadena Unicode inicializada que recibe el destino del vínculo simbólico. Se deben establecer los miembros **MaximumLength** y **buffer** si se produce un error en la llamada.

</dd> <dt>

*ReturnedLength* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe la longitud de la cadena Unicode devuelta en el parámetro *LinkTarget* . Si la función devuelve **un \_ búfer de estado \_ demasiado \_ pequeño**, esta variable recibe el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el **estado \_ correcto** o un estado de error.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
