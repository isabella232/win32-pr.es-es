---
title: Método ChangeRole de la Win32_TSLicenseServer clase
description: Cambia el ámbito de detección del Escritorio remoto de licencias. El ámbito de detección determina qué Escritorio remoto host de sesión (host de sesión de Escritorio remoto) de la red pueden detectar automáticamente el servidor de licencias.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Método ChangeRole Servicios de Escritorio remoto
- Método ChangeRole Servicios de Escritorio remoto , Win32_TSLicenseServer clase
- Win32_TSLicenseServer clase Servicios de Escritorio remoto , método ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891316"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Método ChangeRole de la clase \_ TSLicenseServer de Win32

Cambia el ámbito de detección del Escritorio remoto de licencias. El ámbito de detección determina qué Escritorio remoto host de sesión (host de sesión de Escritorio remoto) de la red pueden detectar automáticamente el servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServerRole* \[ En\]
</dt> <dd>

Ámbito de detección del Escritorio remoto de licencias. Puede establecer uno de los siguientes valores.

<dt>

0
</dt> <dd>

Los servidores host de sesión de Escritorio remoto del mismo grupo de trabajo pueden detectar el servidor de licencias.

</dd> <dt>

1
</dt> <dd>

Los servidores host de sesión de Escritorio remoto del mismo dominio pueden detectar el servidor de licencias. Debe haber iniciado sesión como administrador de dominio para establecer este valor.

</dd> <dt>

2
</dt> <dd>

Los servidores host de sesión de Escritorio remoto de varios dominios del mismo bosque pueden detectar el servidor de licencias. Debe haber iniciado sesión como administrador de empresa para establecer este valor.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

