---
title: Método REVOKE de la clase Win32_TSIssuedLicense
description: Revoca el Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (RDS \ 160; Cal por dispositivo) representadas por el \_ objeto TSIssuedLicense de Win32. No es una función estática.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Método REVOKE Servicios de Escritorio remoto
- Método REVOKE Servicios de Escritorio remoto, clase Win32_TSIssuedLicense
- Clase Win32_TSIssuedLicense Servicios de Escritorio remoto, método REVOKE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803866"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a>Método REVOKE de la \_ clase Win32 TSIssuedLicense

Revoca el Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (cal por dispositivo de RDS) representadas por el objeto [**\_ TSIssuedLicense de Win32**](win32-tsissuedlicense.md) . No es una función estática.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RevokableCals* \[ enuncia\]
</dt> <dd>

Número de cal de RDS del mismo tipo que el objeto actual que se puede revocar.

</dd> <dt>

*NextRevokeAllowedOn* \[ enuncia\]
</dt> <dd>

Fecha en la que el administrador puede intentar revocar las licencias. Este parámetro solo contiene datos válidos cuando se ha producido un error en la llamada al método **REVOKE** porque se ha alcanzado el número máximo de revocación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Solo se pueden revocar las cal por dispositivo de RDS.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> </dl>

 

