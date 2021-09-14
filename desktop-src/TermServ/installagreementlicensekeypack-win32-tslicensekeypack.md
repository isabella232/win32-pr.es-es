---
title: Método InstallAgreementLicenseKeyPack de la Win32_TSLicenseKeyPack clase
description: Instala un paquete Servicios de Escritorio remoto de claves de licencia que se compró a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Método InstallAgreementLicenseKeyPack Servicios de Escritorio remoto
- Método InstallAgreementLicenseKeyPack Servicios de Escritorio remoto , Win32_TSLicenseKeyPack clase
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto método , InstallAgreementLicenseKeyPack
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168694"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método InstallAgreementLicenseKeyPack de la clase TSLicenseKeyPack de Win32 \_

Instala un paquete Servicios de Escritorio remoto de claves de licencia que se compró a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.

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

*AgreementType* \[ En\]

Tipo de contrato.

| Value | Descripción |
|-------|-------------|
| 0 | El paquete de claves de licencia es de un contrato seleccionar licencia por volumen (para clientes con 250 o más equipos). El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado. |
| 1 | El paquete de claves de licencia es de un Enterprise de licencia por volumen para clientes con 250 o más equipos. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado. |
| 2 | El paquete de claves de licencia es de un contrato de licencia por volumen de Campus para una institución de educación superior. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado. |
| 3 | El paquete de claves de licencia es de un contrato de licencia por volumen educativo para las instituciones primarias y secundarias. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado. |
| 4 | El paquete de claves de licencia es de un contrato de licencia del proveedor de servicios para que los proveedores de servicios licencian software de Microsoft mensualmente. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado. |
| 5 | El paquete de claves de licencia es de otro contrato de licencia, como Open Value, Multi-Year Open License y Open Subscription License. El *parámetro sAgreementNumber* es el número de contrato proporcionado con la información del programa. |

*sAgreementNumber* \[ En\]

Número de contrato o número de inscripción. El *parámetro sAgreementNumber* es una cadena numérica de siete dígitos sin guiones.

*ProductVersion* \[ En\]

Versión del producto.

| Value | Descripción |
|-------|-------------|
| 0 | No compatible |
| 1 | No compatible |
| 2 | Windows Server 2008/Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[ En\]

Tipo de producto.

| Value | Descripción |
|-------|-------------|
| 0 | El Servicios de Escritorio remoto de producto del paquete de claves de licencia es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de Escritorio remoto debe tener una licencia. |
| 1 | El Servicios de Escritorio remoto de producto del paquete de claves de licencia es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de Escritorio remoto debe tener una licencia. |
| 2 | Este tipo de producto no es válido. |

*LicenseCount* \[ En\]

Número de licencias que se instalarán.

*KeyPackId* \[ out\]

Recibe el identificador del paquete de claves.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

