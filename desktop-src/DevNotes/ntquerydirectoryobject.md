---
description: Recupera información sobre el objeto de directorio especificado.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Función NtQueryDirectoryObject
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
ms.openlocfilehash: 11c7240cf63fa2f7e13338a0e0459e172e41aa1ed71db90c661b8aad0915d670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079675"
---
# <a name="ntquerydirectoryobject-function"></a>Función NtQueryDirectoryObject

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

*DirectoryHandle* \[ En\]
</dt> <dd>

Identificador del objeto de directorio.

</dd> <dt>

*Búfer* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer que recibe la información del directorio. Este búfer recibe una o varias estructuras **OBJECT \_ DIRECTORY \_ INFORMATION,** la última es **NULL,** seguida de cadenas que contienen los nombres de las entradas del directorio. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*Longitud* \[ En\]
</dt> <dd>

Tamaño del búfer de salida proporcionado por el usuario, en bytes.

</dd> <dt>

*ReturnSingleEntry* \[ En\]
</dt> <dd>

Indica si la función debe devolver solo una sola entrada.

</dd> <dt>

*RestartScan* \[ En\]
</dt> <dd>

Indica si se debe reiniciar el examen o continuar con la enumeración utilizando la información pasada en el *parámetro Context.*

</dd> <dt>

*Contexto* \[ in, out\]
</dt> <dd>

Contexto de enumeración.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe la longitud de la información del directorio devuelta en el búfer de salida, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **STATUS \_ SUCCESS o** un estado de error.

## <a name="remarks"></a>Comentarios

A continuación se muestra la definición de la **estructura OBJECT \_ DIRECTORY \_ INFORMATION.**

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
