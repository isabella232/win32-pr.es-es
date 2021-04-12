---
title: Método InstallOpenLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Instala una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Método InstallOpenLicenseKeyPack Servicios de Escritorio remoto
- Método InstallOpenLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método InstallOpenLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489838"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método InstallOpenLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32

Instala una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.

## <a name="syntax"></a>Sintaxis


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Parámetros

*sLicenseNumber* \[ de\]

cadena numérica de 8 caracteres que se proporciona con el paquete de claves de licencia. El parámetro *sLicenseNumber* no puede contener guiones.

*sAuthorizationNumber* \[ de\]

cadena alfanumérica de 15 caracteres que se proporciona con la clave de licencia. El parámetro *sAuthorizationNumber* no puede contener guiones.

*ProductVersion* \[ de\]

Versión del producto.

| Value | Descripción |
|-------|-------------|
| 0 | No compatible |
| 1 | No compatible |
| 2 | Windows Server 2008/Windows Server 2008 R2 |
| 4 | Windows Server 2012 o Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[ de\]
</dt> <dd>

Tipo de producto.

| Value | Descripción |
|-------|-------------|
| 0 | El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia. |
| 1 | El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia. |
| 2 | Este tipo de producto no es válido. |

*LicenseCount* \[ de\]

El número de licencias que se van a instalar.

*KeyPackId* \[ enuncia\]

Recibe el identificador del paquete de claves.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

