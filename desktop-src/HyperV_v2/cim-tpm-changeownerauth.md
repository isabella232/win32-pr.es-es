---
description: Cambia la credencial de autorización de propietario del dispositivo TPM. Se requieren las contraseñas de autorización de propietarios antiguas y nuevas.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Método ChangeOwnerAuth de la CIM_TPM clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a92911bcf9c2739d34e8b7602ab5f4cb0032fe5a77376632063971b88f2101d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646667"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>Método ChangeOwnerAuth de la clase TPM de CIM \_

Cambia la credencial de autorización de propietario del dispositivo TPM. Se requieren las contraseñas de autorización de propietarios antiguas y nuevas.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OldOwnerAuth* \[ En\]
</dt> <dd>

Representa la credencial de autorización de propietario antigua necesaria para tomar posesión del dispositivo TPM. La **\_ subclase SharedCredential** de CIM puede ser necesaria con un valor distinto de NULL de **CIM \_ SharedCredential.****Propiedad** secreta para el parámetro .

</dd> <dt>

*NewOwnerAuth* \[ En\]
</dt> <dd>

Representa la nueva credencial de autorización de propietario necesaria para tomar posesión del dispositivo TPM. La **\_ subclase SharedCredential** de CIM puede ser necesaria con un valor distinto de NULL de **CIM \_ SharedCredential.****Propiedad** secreta para el parámetro .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error desconocido o no especificado** (2)
</dt> <dt>

**DMTF reservado** (3..4095)
</dt> <dt>

**Método reservado** (4096..32767)
</dt> <dt>

**Proveedor especificado** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM \_ de CIM**](cim-tpm.md)
</dt> </dl>

 

 




