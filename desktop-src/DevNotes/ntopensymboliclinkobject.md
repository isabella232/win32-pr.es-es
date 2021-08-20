---
description: Abre un vínculo simbólico existente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Función NtOpenSymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 1713d12763eaaa5c43b4ef27f3d8843eefd3ba86f0a8ddfea9dfaecd9d01b10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003766"
---
# <a name="ntopensymboliclinkobject-function"></a>Función NtOpenSymbolicLinkObject

\[Esta función puede modificarse o no estar disponible en el futuro.\]

Abre un vínculo simbólico existente.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LinkHandle* \[ out\]
</dt> <dd>

Identificador del objeto de vínculo simbólico recién abierto.

</dd> <dt>

*DesiredAccess* \[ En\]
</dt> <dd>

Máscara [**de \_ acceso**](../secauthz/access-mask.md) que especifica el acceso solicitado al objeto de directorio. Es habitual usar GENERIC \_ READ para que el identificador se pueda pasar a la función [**NtQueryDirectoryObject.**](ntquerydirectoryobject.md)

</dd> <dt>

*ObjectAttributes* \[ En\]
</dt> <dd>

Atributos del objeto de directorio. Para inicializar **la estructura OBJECT \_ ATTRIBUTES,** use la macro **InitializeObjectAttributes.** Si el autor de la llamada no se ejecuta en un contexto de subproceso del sistema, debe especificar la marca **OBJ \_ KERNEL \_ HANDLE** al inicializar la estructura. Para obtener más información, consulte la documentación de estos elementos en la documentación de WDK.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **STATUS \_ SUCCESS o** un estado de error.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
