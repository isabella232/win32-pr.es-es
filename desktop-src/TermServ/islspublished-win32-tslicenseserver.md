---
title: Método IsLSPublished de la Win32_TSLicenseServer clase
description: Recupera si el Escritorio remoto de licencias de servidor de licencias se publica en Active Directory Domain Services (AD \ 160;DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Método IsLSPublished Servicios de Escritorio remoto
- Método IsLSPublished Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto método , IsLSPublished
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a5ca1fd4159b5b632dde5930f25b28ccbc7fcbad41ee2ee2da126252c6eb086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000655"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a>Método IsLSPublished de la clase TSLicenseServer de Win32 \_

Recupera si el servidor de Escritorio remoto licencia está publicado en Active Directory Domain Services (AD DS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Publicado* \[ out\]
</dt> <dd>

Valor booleano que indica si el servidor de licencias está publicado en AD DS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Si el servidor de licencias se publica en AD DS, los servidores de host de sesión de Escritorio remoto (Host de sesión de Escritorio remoto) del mismo bosque lo detectarán automáticamente.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSLicenseServer de Win32 \_**](win32-tslicenseserver.md)
</dt> </dl>

 

