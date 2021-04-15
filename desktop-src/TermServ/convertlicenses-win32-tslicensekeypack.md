---
title: Método ConvertLicenses de la clase Win32_TSLicenseKeyPack
description: Convierte las licencias en el paquete de claves actual.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Método ConvertLicenses Servicios de Escritorio remoto
- Método ConvertLicenses Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ConvertLicenses
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
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422024"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Método ConvertLicenses de la \_ clase TSLicenseKeyPack de Win32

Convierte las licencias en el paquete de claves actual. Si se trata de una licencia por usuario, se convierte en una licencia por dispositivo. Si la licencia es una licencia por dispositivo, se convierte en una licencia por usuario.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Recuento* \[ de\]
</dt> <dd>

El número de licencias que se van a convertir.

</dd> <dt>

*KeypackID* \[ enuncia\]
</dt> <dd>

Identificador del paquete de claves resultante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





