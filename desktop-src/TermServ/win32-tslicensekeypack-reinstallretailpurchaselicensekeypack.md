---
title: Método ReinstallRetailPurchaseLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta directa.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Método ReinstallRetailPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método ReinstallRetailPurchaseLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ReinstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078963"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ReinstallRetailPurchaseLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32

Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta directa.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sLicenseCode* \[ de\]
</dt> <dd>

Contiene el código de licencia de 25 caracteres. Solo se debe proporcionar como entrada la cadena de caracteres alfanuméricos de 25 caracteres. No se deben agregar guiones.

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

 

 





