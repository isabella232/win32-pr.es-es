---
description: Recupera información sobre el objeto de directorio especificado.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649629"
---
# <a name="ntquerydirectoryobject-function"></a>NtQueryDirectoryObject función)

\[Esta función puede modificarse o no estar disponible en el futuro.\]

Recupera información sobre el objeto de directorio especificado.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DirectoryHandle* \[ de\]
</dt> <dd>

Identificador del objeto de directorio.

</dd> <dt>

*Búfer* \[ de out, opcional\]
</dt> <dd>

Un puntero a un búfer que recibe la información de directorio. Este búfer recibe una o más estructuras de **\_ \_ información de directorio de objetos** , la última, que es **null**, y las cadenas que contienen los nombres de las entradas de directorio. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*Longitud* \[ de\]
</dt> <dd>

Tamaño del búfer de salida proporcionado por el usuario, en bytes.

</dd> <dt>

*ReturnSingleEntry* \[ de\]
</dt> <dd>

Indica si la función debe devolver una sola entrada.

</dd> <dt>

*RestartScan* \[ de\]
</dt> <dd>

Indica si se debe reiniciar el examen o continuar la enumeración con la información pasada en el parámetro de *contexto* .

</dd> <dt>

*Contexto* \[ de in, out\]
</dt> <dd>

Contexto de la enumeración.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe la longitud de la información de directorio devuelta en el búfer de salida, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el **estado \_ correcto** o un estado de error.

## <a name="remarks"></a>Observaciones

La siguiente es la definición de la estructura de **\_ \_ información de directorio de objetos** .

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
