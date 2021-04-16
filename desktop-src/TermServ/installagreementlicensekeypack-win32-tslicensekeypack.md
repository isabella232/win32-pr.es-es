---
title: Método InstallAgreementLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Método InstallAgreementLicenseKeyPack Servicios de Escritorio remoto
- Método InstallAgreementLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686174"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método InstallAgreementLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32

Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.

## <a name="syntax"></a>Sintaxis


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Parámetros

*AgreementType* \[ de\]

Tipo de contrato.

| Value | Descripción |
|-------|-------------|
| 0 | El paquete de claves de licencia procede de un contrato de licencia por volumen Select (para clientes con 250 o más equipos). El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado. |
| 1 | El paquete de claves de licencia procede de un contrato de licencia por volumen empresarial para clientes con 250 o más equipos. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado. |
| 2 | El paquete de claves de licencia procede de un contrato de licencia por volumen de campus para una institución de educación superior. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado. |
| 3 | El paquete de claves de licencia proviene de un contrato de licencia por volumen escolar para instituciones principales y secundarias. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado. |
| 4 | El paquete de claves de licencia procede de un contrato de licencia de proveedor de servicios para que los proveedores de servicios de licencias de software de Microsoft se basen mensualmente. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado. |
| 5 | El paquete de claves de licencia procede de otro contrato de licencia, como un valor abierto, una licencia Open de varios años y una licencia de suscripción abierta. El parámetro *sAgreementNumber* es el número de contrato proporcionado con la información del programa. |

*sAgreementNumber* \[ de\]

Número de contrato o número de inscripción. El parámetro *sAgreementNumber* es una cadena numérica de siete dígitos sin guiones.

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

Tipo de producto.

| Value | Descripción |
|-------|-------------|
| 0 | El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia. |
| 1 | El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia. |
| 2 | Este tipo de producto no es válido. |

*LicenseCount* \[ de\]

Número de licencias que se van a instalar.

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

 

