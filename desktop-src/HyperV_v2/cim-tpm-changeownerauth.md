---
description: Cambia la credencial de autorización de propietario del dispositivo de TPM. Se requieren las contraseñas de autorización de propietario antiguas y nuevas.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Método ChangeOwnerAuth de la clase CIM_TPM
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
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687350"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>Método ChangeOwnerAuth de la \_ clase TPM CIM

Cambia la credencial de autorización de propietario del dispositivo de TPM. Se requieren las contraseñas de autorización de propietario antiguas y nuevas.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OldOwnerAuth* \[ de\]
</dt> <dd>

Representa la antigua credencial de autorización de propietario necesaria para tomar posesión del dispositivo de TPM. La subclase **CIM \_ SharedCredential** puede ser necesaria con un valor distinto de NULL de **la \_ SharedCredential CIM**.**Propiedad Secret** del parámetro.

</dd> <dt>

*NewOwnerAuth* \[ de\]
</dt> <dd>

Representa la nueva credencial de autorización de propietario necesaria para tomar posesión del dispositivo de TPM. La subclase **CIM \_ SharedCredential** puede ser necesaria con un valor distinto de NULL de **la \_ SharedCredential CIM**.**Propiedad Secret** del parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error desconocido o no especificado** (2)
</dt> <dt>

**DMTF reservado** (3.. 4095)
</dt> <dt>

**Método reservado** (4096.. 32767)
</dt> <dt>

**Proveedor especificado** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de CIM \_**](cim-tpm.md)
</dt> </dl>

 

 




