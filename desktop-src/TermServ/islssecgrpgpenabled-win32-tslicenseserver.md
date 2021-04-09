---
title: Método IsLSSecGrpGPEnabled de la clase Win32_TSLicenseServer
description: Recupera si el grupo de seguridad del servidor de licencias \ 0034; \ 0034; la configuración de directiva de grupo está habilitada en el servidor de licencias de Escritorio remoto.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Método IsLSSecGrpGPEnabled Servicios de Escritorio remoto
- Método IsLSSecGrpGPEnabled Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSSecGrpGPEnabled
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
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150493"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Método IsLSSecGrpGPEnabled de la \_ clase TSLicenseServer de Win32

Recupera si el valor de directiva de grupo "grupo de seguridad del servidor de licencias" está habilitado en el servidor de licencias de Escritorio remoto.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Habilitado* \[ enuncia\]
</dt> <dd>

Valor booleano que indica si está habilitada la configuración de directiva "grupo de seguridad del servidor de licencias".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

La configuración de directiva "grupo de seguridad del servidor de licencias" le permite especificar los servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) que pueden ponerse en contacto con el servidor de licencias para obtener Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS). Si la configuración de directiva está habilitada en el servidor de licencias, el servidor solo responderá a las solicitudes CAL de RDS de los servidores host de sesión de escritorio remoto cuyas cuentas de equipo sean miembros del grupo local de Terminal Server equipos en el servidor de licencias.

La configuración de Directiva se encuentra en el siguiente nodo del editor de directivas de grupo local:

Configuración del equipo \\ plantillas administrativas \\ componentes de Windows \\ Terminal Services licencias de \\ TS

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
</dt> </dl>

 

