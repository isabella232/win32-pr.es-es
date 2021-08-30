---
title: Método GetLicenseServerId de la Win32_TSLicenseServer clase
description: Recupera el identificador Escritorio remoto servidor de licencias si el servidor está activado actualmente.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- Método GetLicenseServerId Servicios de Escritorio remoto
- Método GetLicenseServerId Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto método , GetLicenseServerId
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b104de72c70e43a2c2e115f3ac2a770f1d323c6270f259aae53aa49c91aa2bc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080095"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a>Método GetLicenseServerId de la clase TSLicenseServer de Win32 \_

Recupera el identificador Escritorio remoto servidor de licencias si el servidor está activado actualmente.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sLicenseServerId* \[ out\]
</dt> <dd>

Escritorio remoto de servidor de licencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

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

[**TSLicenseServer de Win32 \_**](win32-tslicenseserver.md)
</dt> </dl>

 

