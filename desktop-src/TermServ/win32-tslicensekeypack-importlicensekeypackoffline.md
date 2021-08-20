---
title: Método ImportLicenseKeyPackOffline de la Win32_TSLicenseKeyPack clase
description: Importa, desde otro servidor Escritorio remoto licencias, un Servicios de Escritorio remoto de claves de licencia que usa un identificador de licencia que se recibió a través de Internet o el teléfono.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Método ImportLicenseKeyPackOffline Servicios de Escritorio remoto
- Método ImportLicenseKeyPackOffline Servicios de Escritorio remoto , Win32_TSLicenseKeyPack clase
- Win32_TSLicenseKeyPack clase Servicios de Escritorio remoto método , ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7d5be5dc8cfd9f654c09d989149a423351689f420a52ca1756fb197260e800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348636"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Método ImportLicenseKeyPackOffline de la clase \_ TSLicenseKeyPack de Win32

Importa, desde otro servidor Escritorio remoto licencias, un Servicios de Escritorio remoto de claves de licencia que usa un identificador de licencia que se recibió a través de Internet o el teléfono.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sLicenseKeyPackId* \[ En\]
</dt> <dd>

Contiene el código de licencia de 35 caracteres. Solo se debe dar como entrada la cadena de caracteres alfanuméricos de 35 caracteres. No se debe agregar ningún guion.

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

 

 





