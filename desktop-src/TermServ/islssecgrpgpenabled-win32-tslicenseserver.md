---
title: Método IsLSSecGrpGPEnabled de la Win32_TSLicenseServer clase
description: Recupera si \ 0034;grupo de seguridad del servidor de licencias \ 0034; la configuración de directiva de grupo está habilitada en Escritorio remoto servidor de licencias.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Método IsLSSecGrpGPEnabled Servicios de Escritorio remoto
- Método IsLSSecGrpGPEnabled Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto método , IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688843106583ea0ca32a3cc8ac7142d51aac737ad6722ab4ef95621b63b66eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138368"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Método IsLSSecGrpGPEnabled de la clase TSLicenseServer de Win32 \_

Recupera si la configuración de directiva de grupo "grupo de seguridad del servidor de licencias" está habilitada en Escritorio remoto servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Habilitado* \[ out\]
</dt> <dd>

Valor booleano que indica si la configuración de directiva "Grupo de seguridad del servidor de licencias" está habilitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

La configuración de directiva "grupo de seguridad del servidor de licencias" permite especificar los servidores de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) que pueden ponerse en contacto con el servidor de licencias para obtener licencias de acceso de cliente (CAL de RDS) de Servicios de Escritorio remoto. Si la configuración de directiva está habilitada en el servidor de licencias, el servidor solo responderá a las solicitudes cal de RDS de los servidores host de sesión de Escritorio remoto cuyas cuentas de equipo son miembros del grupo local Equipos de Terminal Server en el servidor de licencias.

La configuración de directiva se encuentra en el siguiente nodo del editor de directivas de grupo local:

Configuración del \\ equipo Plantillas administrativas Windows licencias de \\ \\ TS de Terminal Services \\ para componentes de equipo

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

 

