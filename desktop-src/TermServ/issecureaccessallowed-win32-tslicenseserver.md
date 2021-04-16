---
title: Método IsSecureAccessAllowed de la clase Win32_TSLicenseServer
description: Recupera si se permite que un servidor host de sesión de escritorio remoto (host de sesión Escritorio remoto de RD) solicite Servicios de Escritorio remoto licencias de acceso de cliente (RDS \ 160; Cal) del servidor de licencias de Escritorio remoto.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Método IsSecureAccessAllowed Servicios de Escritorio remoto
- Método IsSecureAccessAllowed Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsSecureAccessAllowed
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
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534126"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>Método IsSecureAccessAllowed de la \_ clase TSLicenseServer de Win32

Recupera si se permite que un servidor host de sesión de escritorio remoto (host de sesión Escritorio remoto de RD) solicite Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) del servidor de licencias de Escritorio remoto.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tsname* \[ de\]
</dt> <dd>

Nombre del servidor host de sesión de escritorio remoto.

</dd> <dt>

*Permitido* \[ enuncia\]
</dt> <dd>

Valor booleano que indica si el servidor host de sesión de escritorio remoto puede solicitar cal de RDS del servidor de licencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

El valor devuelto se basa en la configuración de directiva de grupo "grupo de seguridad del servidor de licencias" y la pertenencia al grupo local de Terminal Server equipos en el servidor de licencias de Escritorio remoto.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

