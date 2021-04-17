---
description: Abre un vínculo simbólico existente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject función)
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
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671023"
---
# <a name="ntopensymboliclinkobject-function"></a>NtOpenSymbolicLinkObject función)

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

*LinkHandle* \[ enuncia\]
</dt> <dd>

Identificador del objeto de vínculo simbólico recién abierto.

</dd> <dt>

*DesiredAccess* \[ de\]
</dt> <dd>

Una [**\_ máscara de acceso**](../secauthz/access-mask.md) que especifica el acceso solicitado al objeto de directorio. Es habitual utilizar \_ la lectura genérica para que el identificador se pueda pasar a la función [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .

</dd> <dt>

*ObjectAttributes* \[ de\]
</dt> <dd>

Atributos del objeto de directorio. Para inicializar la estructura de **\_ atributos de objeto** , use la macro **InitializeObjectAttributes** . Si el llamador no se está ejecutando en un contexto de subproceso del sistema, debe especificar la marca de **\_ \_ identificador de kernel de obj** al inicializar la estructura. Para obtener más información, consulte la documentación de estos elementos en la documentación del WDK.

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

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
