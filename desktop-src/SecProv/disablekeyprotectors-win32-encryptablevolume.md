---
description: Deshabilita o suspende todos los protectores de clave asociados a este volumen.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Método DisableKeyProtectors de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253448"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método DisableKeyProtectors de la clase EncryptableVolume de Win32 \_

El **método DisableKeyProtectors** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) deshabilita o suspende todos los protectores de clave asociados a este volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DisableCount* \[ en, opcional\]
</dt> <dd>

Tipo: **uint32**

Entero que especifica el número de reinicios para los que se deshabilitarán los protectores de clave. Este parámetro solo está disponible en volúmenes del sistema operativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="security-considerations"></a>Consideraciones de seguridad

Este método expone la clave de cifrado del volumen sin cifrar en el disco duro, desactivando cualquier protección del volumen. Se recomienda no tener ninguna contraseña o clave de cifrado en texto no cifrado.

## <a name="remarks"></a>Observaciones

Se pueden agregar nuevos protectores de clave incluso cuando los protectores de clave están deshabilitados o suspendidos. Estos protectores de clave permanecerán deshabilitados a menos que se llame a [**EnableKeyProtectors.**](enablekeyprotectors-win32-encryptablevolume.md)

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
