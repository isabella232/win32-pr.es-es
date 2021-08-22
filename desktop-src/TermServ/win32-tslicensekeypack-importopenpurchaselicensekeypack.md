---
title: Método ImportOpenPurchaseLicenseKeyPack de la Win32_TSLicenseKeyPack clase
description: Importa, desde otro servidor Escritorio remoto licencias, un paquete de claves de licencia Servicios de Escritorio remoto licencia abierta.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Método ImportOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método ImportOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto , Win32_TSLicenseKeyPack clase
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto , método ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768961bda04776a73d0aa74422ce0ed5088e041ee41e4732becd72914dcabf04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008475"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ImportOpenPurchaseLicenseKeyPack de la clase TSLicenseKeyPack de Win32 \_

Importa, desde otro servidor Escritorio remoto licencias, un paquete de claves de licencia Servicios de Escritorio remoto licencia abierta.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
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

*sLicenseNumber* \[ En\]
</dt> <dd>

Cadena numérica de 8 caracteres que se proporciona con el paquete de claves de licencia. El *parámetro sLicenseNumber* no puede contener guiones.

</dd> <dt>

*sAuthorizationNumber* \[ En\]
</dt> <dd>

Cadena alfanumérica de 15 caracteres que se proporciona con la clave de licencia. El *parámetro sAuthorizationNumber* no puede contener guiones.

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

Número de licencias que se importarán

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

 

 





