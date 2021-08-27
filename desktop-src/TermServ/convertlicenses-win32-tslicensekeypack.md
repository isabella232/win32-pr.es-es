---
title: Método ConvertLicenses de la Win32_TSLicenseKeyPack clase
description: Convierte las licencias del paquete de claves actual.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Método ConvertLicenses Servicios de Escritorio remoto
- Método ConvertLicenses Servicios de Escritorio remoto , Win32_TSLicenseKeyPack clase
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto método , ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfb65ea7429af14e633c8dee655b4977427e3a685e1404856fd9b5f2daf2ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099575"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Método ConvertLicenses de la clase TSLicenseKeyPack de Win32 \_

Convierte las licencias del paquete de claves actual. Si la licencia es una licencia por usuario, se convierte en una licencia por dispositivo. Si la licencia es una licencia por dispositivo, se convierte en una licencia por usuario.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Recuento* \[ En\]
</dt> <dd>

Número de licencias que se va a convertir.

</dd> <dt>

*KeypackID* \[ out\]
</dt> <dd>

Identificador del paquete de claves resultante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





