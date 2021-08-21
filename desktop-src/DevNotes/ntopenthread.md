---
description: Abre un identificador para un objeto de subproceso con el acceso especificado.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Función NtOpenThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e5f459b12d90a12b7c75aabd44d25f6fcf352aff8914e6d991471acaee400260
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079695"
---
# <a name="ntopenthread-function"></a>Función NtOpenThread

\[Esta función se puede cambiar o quitar de Windows sin previo aviso. En su [**lugar, use la función OpenThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)\]

Abre un identificador para un objeto de subproceso con el acceso especificado.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ThreadHandle* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el identificador de objeto de subproceso.

</dd> <dt>

*DesiredAccess* \[ En\]
</dt> <dd>

Tipo [**de datos ACCESS \_ MASK**](../secauthz/access-mask-format.md) que proporciona los tipos de acceso deseados para el objeto de subproceso.

</dd> <dt>

*ObjectAttributes* \[ En\]
</dt> <dd>

Puntero a una [estructura OBJECT \_ ATTRIBUTES.](https://msdn.microsoft.com/library/aa491657.aspx) El **miembro ObjectName** de esta estructura debe ser NULL.

**Windows Server 2003 y Windows XP:** El **miembro ObjectName** de esta estructura puede apuntar a un nombre de objeto. Si **ObjectName** no es NULL, el *parámetro ClientId* debe ser NULL.

</dd> <dt>

*ClientId* \[ En\]
</dt> <dd>

Puntero a una estructura **de \_ identificador de** cliente que identifica el subproceso cuyo subproceso se va a abrir.

**Windows Server 2003 y Windows XP:** Puntero a una estructura **de \_ identificador de** cliente que identifica el subproceso cuyo subproceso se va a abrir. Este parámetro puede ser NULL. Si este parámetro no es NULL, el **miembro ObjectName** de la estructura a la que apunta el parámetro *ObjectAttributes* debe ser NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **NTSTATUS o** un código de error.

Los formularios y la importancia de los códigos de error **NTSTATUS** se enumeran en el archivo de encabezado Ntstatus.h disponible en WDK y se describen en la documentación de WDK.

## <a name="remarks"></a>Comentarios

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, Ntdll.lib, está disponible en WDK. También puede usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
