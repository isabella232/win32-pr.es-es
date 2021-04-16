---
title: Método IsLSPublished de la clase Win32_TSLicenseServer
description: Recupera si el servidor de licencias de Escritorio remoto se publica en Active Directory Domain Services (AD \ 160; DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Método IsLSPublished Servicios de Escritorio remoto
- Método IsLSPublished Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSPublished
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
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676813"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a>Método IsLSPublished de la \_ clase TSLicenseServer de Win32

Recupera si el servidor de licencias de Escritorio remoto se publica en Active Directory Domain Services (AD DS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Publicado* \[ por enuncia\]
</dt> <dd>

Valor booleano que indica si el servidor de licencias está publicado en AD DS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Si el servidor de licencias está publicado en AD DS, se detectará Escritorio remoto automáticamente en los servidores host de sesión de escritorio remoto (host de sesión de RD) del mismo bosque.

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

 

