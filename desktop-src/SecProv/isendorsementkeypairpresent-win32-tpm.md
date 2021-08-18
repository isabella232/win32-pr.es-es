---
description: El método IsEndorsementKeyPairPresent de la clase Tpm de Win32 indica si el par de claves de aprobación \_ existe en el dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Método IsEndorsementKeyPairPresent de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: bcbc0c4877aae2db0e94d42838100720ee0ae0dcbdcc33f52cf70d2e23327e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004473"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Método IsEndorsementKeyPairPresent de la clase Tpm de \_ Win32

El **método IsEndorsementKeyPairPresent** de la clase [**\_ Tpm de Win32**](win32-tpm.md) indica si el par de claves de aprobación existe en el dispositivo. El par de claves de aprobación es necesario antes de que el dispositivo pueda ser propiedad de . El método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) puede crear este par de claves.

El dispositivo debe estar habilitado y activado para que este método se pueda realizar correctamente. Para habilitar y activar un dispositivo sin tener en cuenta, consulte el [**método SetPhysicalPresenceRequest.**](setphysicalpresencerequest-win32-tpm.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsEndorsementKeyPairPresent* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** el par de claves de aprobación existe en el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
