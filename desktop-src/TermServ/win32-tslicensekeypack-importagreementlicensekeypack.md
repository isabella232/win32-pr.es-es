---
title: Método ImportAgreementLicenseKeyPack de la Win32_TSLicenseKeyPack clase
description: Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia de Servicios de Escritorio remoto que se adquirió a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Método ImportAgreementLicenseKeyPack Servicios de Escritorio remoto
- Método ImportAgreementLicenseKeyPack Servicios de Escritorio remoto , Win32_TSLicenseKeyPack clase
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto , método ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b911a722f4f26aaf83debcb70413cb9dad2b40d2ca12b4ad3310aee4510ca1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603808"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ImportAgreementLicenseKeyPack de la clase TSLicenseKeyPack de Win32 \_

Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia de Servicios de Escritorio remoto que se adquirió a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AgreementType* \[ En\]
</dt> <dd>

Tipo de contrato.

<dt>

0
</dt> <dd>

El paquete de claves de licencia es de un contrato de licencia select volume (para clientes con 250 o más equipos). El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado.

</dd> <dt>

1
</dt> <dd>

El paquete de claves de licencia es de un Enterprise de licencia por volumen para clientes con 250 o más equipos. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado.

</dd> <dt>

2
</dt> <dd>

El paquete de claves de licencia es de un contrato de licencia por volumen de Campus para una institución de educación superior. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado.

</dd> <dt>

3
</dt> <dd>

El paquete de claves de licencia es de un contrato de licencia por volumen educativo para las instituciones primarias y secundarias. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado.

</dd> <dt>

4
</dt> <dd>

El paquete de claves de licencia es de un contrato de licencia del proveedor de servicios para que los proveedores de servicios licencian software de Microsoft mensualmente. El *parámetro sAgreementNumber es* el número de inscripción (siete dígitos numéricos) que se encuentra en el formulario del contrato firmado.

</dd> <dt>

5
</dt> <dd>

El paquete de claves de licencia es de otro contrato de licencia, como Open Value, Multi-Year Open License y Open Subscription License. El *parámetro sAgreementNumber* es el número de contrato proporcionado con la información del programa.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ En\]
</dt> <dd>

Número de contrato o número de inscripción. El *parámetro sAgreementNumber* es una cadena numérica de siete dígitos sin guiones.

</dd> <dt>

*ProductVersion* \[ En\]
</dt> <dd>

Versión del producto.

<dt>

0
</dt> <dd>

No compatible.

</dd> <dt>

1
</dt> <dd>

No compatible.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ En\]
</dt> <dd>

Tipo de producto.

<dt>

0
</dt> <dd>

El Servicios de Escritorio remoto de producto del paquete de claves de licencia es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de Escritorio remoto debe tener una licencia.

</dd> <dt>

1
</dt> <dd>

El Servicios de Escritorio remoto de producto del paquete de claves de licencia es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de Escritorio remoto debe tener una licencia.

</dd> <dt>

2
</dt> <dd>

Este tipo de producto no es válido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ En\]
</dt> <dd>

Número de licencias que se importarán.

</dd> <dt>

*sSourceLSName* \[ En\]
</dt> <dd>

Nombre del servidor de licencias Escritorio remoto origen. Este es el nombre distintivo completo o la dirección IP del servidor.

</dd> <dt>

*sSourceLSProductId* \[ En\]
</dt> <dd>

Identificador Escritorio remoto servidor de licencias. es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Recibe el identificador del paquete de claves.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





