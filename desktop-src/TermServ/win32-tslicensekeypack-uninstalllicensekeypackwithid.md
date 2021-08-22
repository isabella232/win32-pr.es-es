---
title: Método UninstallLicenseKeyPackWithId de la Win32_TSLicenseKeyPack clase
description: Desinstala el Servicios de Escritorio remoto de claves de licencia con el identificador del paquete de claves especificado.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Método UninstallLicenseKeyPackWithId Servicios de Escritorio remoto
- Método UninstallLicenseKeyPackWithId Servicios de Escritorio remoto , Win32_TSLicenseKeyPack clase
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto método , UninstallLicenseKeyPackWithId
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1218ce51beac9e20dd04e2a56d9075b6732d65e17689afaba5ce4d8f6669b1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008445"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a>Método UninstallLicenseKeyPackWithId de la clase \_ TSLicenseKeyPack de Win32

Desinstala el Servicios de Escritorio remoto de claves de licencia con el identificador del paquete de claves especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*KeyPackId* \[ En\]
</dt> <dd>

Identificador del paquete de claves que se desinstalará.

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

 

 





