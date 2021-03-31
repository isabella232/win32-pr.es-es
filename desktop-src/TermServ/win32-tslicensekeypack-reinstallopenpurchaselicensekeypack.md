---
title: Método ReinstallOpenPurchaseLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Vuelve a instalar una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Método ReinstallOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método ReinstallOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ReinstallOpenPurchaseLicenseKeyPack
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
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803602"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ReinstallOpenPurchaseLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32

Vuelve a instalar una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.

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

*sLicenseNumber* \[ de\]
</dt> <dd>

cadena numérica de 8 caracteres que se proporciona con el paquete de claves de licencia. El parámetro *sLicenseNumber* no puede contener guiones.

</dd> <dt>

*sAuthorizationNumber* \[ de\]
</dt> <dd>

cadena alfanumérica de 15 caracteres que se proporciona con la clave de licencia. El parámetro *sAuthorizationNumber* no puede contener guiones.

</dd> <dt>

*ProductVersion* \[ de\]
</dt> <dd>

Versión del producto.

<dt>

0
</dt> <dd>

No se admite.

</dd> <dt>

1
</dt> <dd>

No se admite.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ de\]
</dt> <dd>

Tipo de producto.

<dt>

0
</dt> <dd>

El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.

</dd> <dt>

1
</dt> <dd>

El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.

</dd> <dt>

2
</dt> <dd>

Este tipo de producto no es válido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ de\]
</dt> <dd>

El número de licencias que se van a instalar.

</dd> <dt>

*KeyPackId* \[ enuncia\]
</dt> <dd>

Recibe el identificador del paquete de claves.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

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

 

 





