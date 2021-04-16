---
description: Abre un identificador de un objeto de subproceso con el acceso especificado.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread función)
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
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649837"
---
# <a name="ntopenthread-function"></a>NtOpenThread función)

\[Esta función se puede cambiar o quitar de Windows sin previo aviso. En su lugar, use la función [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]

Abre un identificador de un objeto de subproceso con el acceso especificado.

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

*ThreadHandle* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el identificador del objeto de subproceso.

</dd> <dt>

*DesiredAccess* \[ de\]
</dt> <dd>

Un tipo de datos de [**\_ máscara de acceso**](../secauthz/access-mask-format.md) que proporciona los tipos de acceso deseados para el objeto de subproceso.

</dd> <dt>

*ObjectAttributes* \[ de\]
</dt> <dd>

Puntero a una estructura [de \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) . El miembro **objectname** de esta estructura debe ser null.

**Windows Server 2003 y Windows XP:** El miembro **objectname** de esta estructura puede apuntar a un nombre de objeto. Si **objectname** no es null, el parámetro *CLIENTID* debe ser null.

</dd> <dt>

*ClientID* \[ de\]
</dt> <dd>

Puntero a una estructura **de \_ identificador de cliente** que identifica el subproceso cuyo subproceso se va a abrir.

**Windows Server 2003 y Windows XP:** Puntero a una estructura **de \_ identificador de cliente** que identifica el subproceso cuyo subproceso se va a abrir. Este parámetro puede ser NULL. Si este parámetro no es NULL, el miembro **objectname** de la estructura a la que apunta el parámetro *OBJECTATTRIBUTES* debe ser null.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de error **NTSTATUS** o.

Los formularios y la importancia de los códigos de error de **NTSTATUS** se enumeran en el archivo de encabezado NTSTATUS. h disponible en el WDK y se describen en la documentación de WDK.

## <a name="remarks"></a>Observaciones

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK. También puede utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
