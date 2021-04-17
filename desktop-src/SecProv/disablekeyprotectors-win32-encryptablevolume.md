---
description: Deshabilita o suspende todos los protectores de clave asociados a este volumen.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Método DisableKeyProtectors de la clase Win32_EncryptableVolume
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687570"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método DisableKeyProtectors de la \_ clase EncryptableVolume de Win32

El método **DisableKeyProtectors** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) deshabilita o suspende todos los protectores de clave asociados a este volumen.

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

Tipo: **UInt32**

Entero que especifica el número de reinicios para los que se deshabilitarán los protectores de clave. Este parámetro solo está disponible en los volúmenes del sistema operativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Este método expone la clave de cifrado del volumen sin cifrar en el disco duro, desactivando cualquier protección de volumen. Se recomienda no tener ninguna contraseña o clave de cifrado en texto sin formato.

## <a name="remarks"></a>Observaciones

Se pueden agregar nuevos protectores de clave incluso cuando se deshabilitan o se suspenden los protectores de clave. Estos protectores de clave permanecerán deshabilitados a menos que se llame a [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) .

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
