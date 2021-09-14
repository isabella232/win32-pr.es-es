---
title: Método ActivateServerAutomatic de la Win32_TSLicenseServer clase
description: Activa el servidor Escritorio remoto licencias automáticamente a través de Internet.
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- Método ActivateServerAutomatic Servicios de Escritorio remoto
- Método ActivateServerAutomatic Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto método , ActivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073376"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Método ActivateServerAutomatic de la clase TSLicenseServer de Win32 \_

Activa el servidor Escritorio remoto licencias automáticamente a través de Internet.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

El estado de activación devuelto puede ser uno de los siguientes.

<dt>

0
</dt> <dd>

Se activa Escritorio remoto servidor de licencias.

</dd> <dt>

1
</dt> <dd>

El Escritorio remoto de licencias no está activado.

</dd> <dt>

2
</dt> <dd>

Se produjo un error desconocido. No se sabe si el servidor Escritorio remoto licencias está activado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

Este método produce un error a menos que se **establezcan las** propiedades **FirstName**, LastName , **Company** y **CountryRegion.**

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

 

