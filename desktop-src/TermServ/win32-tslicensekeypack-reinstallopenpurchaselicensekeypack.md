---
title: Método ReinstallOpenPurchaseLicenseKeyPack de la Win32_TSLicenseKeyPack clase
description: Vuelve a instalar un paquete de claves Servicios de Escritorio remoto licencia abierta.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Método ReinstallOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método ReinstallOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto , Win32_TSLicenseKeyPack clase
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto método , ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6519e6eedc187b6db2ee93a776843b0f305430df7ae55e4356ebce4de5ad31d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137828"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ReinstallOpenPurchaseLicenseKeyPack de la clase \_ TSLicenseKeyPack de Win32

Vuelve a instalar un paquete de claves Servicios de Escritorio remoto licencia abierta.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
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

Número de licencias que se instalarán.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Recibe el identificador del paquete de claves.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

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

 

 





