---
title: Método IsSecureAccessAllowed de la Win32_TSLicenseServer clase
description: Recupera si un servidor Escritorio remoto host de sesión (host de sesión de Escritorio remoto) puede solicitar Servicios de Escritorio remoto de acceso de cliente (RDS \ 160; CAL) desde el servidor Escritorio remoto licencias.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Método IsSecureAccessAllowed Servicios de Escritorio remoto
- Método IsSecureAccessAllowed Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto método , IsSecureAccessAllowed
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6109eb363459432d50d54eb8521f0f23bb54a0836c82f92af20a5b83b64f1d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351371"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>Método IsSecureAccessAllowed de la clase TSLicenseServer de Win32 \_

Recupera si un servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) puede solicitar licencias de acceso de cliente (CAL de RDS) Servicios de Escritorio remoto desde el servidor de licencias de Escritorio remoto.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tsname* \[ En\]
</dt> <dd>

Nombre del servidor host de sesión de Escritorio remoto.

</dd> <dt>

*Permitido* \[ out\]
</dt> <dd>

Valor booleano que indica si el servidor host de sesión de Escritorio remoto puede solicitar CAL de RDS desde el servidor de licencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

El valor devuelto se basa en la configuración de directiva de grupo "grupo de seguridad del servidor de licencias" y en la pertenencia al grupo local Equipos de Terminal Server Escritorio remoto servidor de licencias.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSLicenseServer de Win32 \_**](win32-tslicenseserver.md)
</dt> <dt>

[**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

