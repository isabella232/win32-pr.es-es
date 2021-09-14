---
title: Método Revoke de la Win32_TSIssuedLicense clase
description: Revoca las Servicios de Escritorio remoto de acceso de cliente por dispositivo (RDS \ 160; CAL por dispositivo) representadas por el objeto \_ TSIssuedLicense de Win32. No se trata de una función estática.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Revocación del método Servicios de Escritorio remoto
- Método Revoke Servicios de Escritorio remoto , Win32_TSIssuedLicense clase
- Win32_TSIssuedLicense clase Servicios de Escritorio remoto método , Revoke
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374543"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a>Método Revoke de la clase \_ TSIssuedLicense de Win32

Revoca las Servicios de Escritorio remoto de acceso de cliente por dispositivo (CAL de RDS por dispositivo) representadas por el objeto [**\_ TSIssuedLicense de Win32.**](win32-tsissuedlicense.md) No se trata de una función estática.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RevokableCals* \[ out\]
</dt> <dd>

Número de CAL de RDS del mismo tipo que el objeto actual que se puede revocar.

</dd> <dt>

*NextRevokeAllowedOn* \[ out\]
</dt> <dd>

Fecha en que el administrador puede intentar revocar las licencias. Este parámetro solo contiene datos válidos cuando se **ha dado** error en la llamada al método Revoke porque se ha alcanzado el número máximo de revocaciones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Solo se pueden revocar las CAL de RDS por dispositivo.

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

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> </dl>

 

