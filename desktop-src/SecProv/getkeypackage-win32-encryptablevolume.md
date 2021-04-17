---
description: Exporta información que puede ayudar a proteger los datos cifrados cuando la unidad está gravemente dañada y no existen archivos de copia de seguridad de datos.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Método GetKeyPackage de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688158"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyPackage de la \_ clase EncryptableVolume de Win32

El método **GetKeyPackage** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) exporta información que puede ayudar a proteger los datos cifrados cuando la unidad está gravemente dañada y no existen archivos de copia de seguridad de datos.

La información exportada se compone de la clave de cifrado del volumen protegida por un protector de clave del tipo "contraseña numérica" o "clave externa". Para hacer uso de este paquete, también debe guardar la contraseña numérica correspondiente o la clave externa.

> [!IMPORTANT]
> Si decide exportar un paquete de claves, asegúrese de mantener esta información en una ubicación bien protegida. No lleve esta información al equipo. Si este paquete de claves se pierde o se lo roban, deberá descifrar el volumen y volver a cifrarlo mediante una nueva clave.

 

En caso de que se produzca un error en la unidad, existe la herramienta de reparación de BitLocker para ayudar a salvar los datos disponibles. Para obtener más información sobre cómo esta herramienta puede usar el paquete de claves, consulte [Cómo usar la herramienta de reparación de BitLocker para ayudar a recuperar datos de un volumen cifrado en Windows Vista](https://support.microsoft.com/kb/928201).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado. Para exportar un paquete de claves, debe usar un protector de clave de tipo "contraseña numérica" o "clave externa".

</dd> <dt>

*\[ KeyPackage \]* \[fuera de\]
</dt> <dd>

Tipo: **Uint8**

Secuencia de bytes que contiene la clave de cifrado para un volumen, protegida por el protector de clave especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                            | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | El protector de clave proporcionado no existe en el volumen.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido </dl> | El parámetro *VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "contraseña numérica" o "clave externa". Use el método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear un protector de clave del tipo adecuado.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]<br/>                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
