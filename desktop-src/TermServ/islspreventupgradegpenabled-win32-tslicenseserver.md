---
title: Método IsLSPreventUpgradeGPEnabled de la Win32_TSLicenseServer clase
description: Recupera si \ 0034;prevent license upgrade \ 0034; La configuración de directiva de grupo está habilitada en Escritorio remoto servidor de licencias.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Método IsLSPreventUpgradeGPEnabled Servicios de Escritorio remoto
- Método IsLSPreventUpgradeGPEnabled Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , método IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7958df7d153db0abafd8e463f22a181f2e5a639afa5c21cb7529a9cd5c005c5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511704"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>Método IsLSPreventUpgradeGPEnabled de la clase TSLicenseServer de Win32 \_

Recupera si la configuración de directiva de grupo "impedir la actualización de licencias" está habilitada en Escritorio remoto servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Habilitado* \[ out\]
</dt> <dd>

Valor booleano que indica si la configuración de directiva "impedir la actualización de licencia" está habilitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Si la configuración de directiva "impedir la actualización de licencias" está habilitada, el servidor de licencias solo emitirá una CAL de RDS temporal al cliente si no hay disponible una CAL de RDS adecuada para el servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto).

La configuración de directiva se encuentra en el siguiente nodo del editor de directivas de grupo local:

Licencias de \\ \\ \\ \\ TS Plantillas administrativas Windows components terminal services

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

