---
description: Exporta información que puede ayudar a recuperar los datos cifrados cuando la unidad está gravemente dañada y no existen archivos de copia de seguridad de datos.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Método GetKeyPackage de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 777c68bab142fc0f27d9200d2aea1ff0c45c47181d951600dcc96bb0e623b6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892362"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyPackage de la clase EncryptableVolume de Win32 \_

El **método GetKeyPackage** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) exporta información que puede ayudar a recuperar los datos cifrados cuando la unidad está gravemente dañada y no existen archivos de copia de seguridad de datos.

La información exportada consta de la clave de cifrado del volumen protegida por un protector de clave del tipo "Contraseña numérica" o "Clave externa". Para usar este paquete, también debe guardar la contraseña numérica o la clave externa correspondientes.

> [!IMPORTANT]
> Si decide exportar un paquete de claves, asegúrese de mantener esta información en una ubicación bien protegida. No lleve esta información al equipo. Si se pierde o se roba este paquete de claves, deberá descifrar el volumen y volver a cifrarlo mediante una nueva clave.

 

En caso de error en la unidad, existe la herramienta de reparación de BitLocker para ayudar a recuperar los datos disponibles. Para obtener más información sobre cómo esta herramienta puede usar el paquete de claves, vea Cómo usar la herramienta de reparación de [BitLocker](https://support.microsoft.com/kb/928201)para ayudar a recuperar datos de un volumen cifrado en Windows Vista .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado. Para exportar un paquete de claves, debe usar un protector de clave de tipo "Contraseña numérica" o "Clave externa".

</dd> <dt>

*KeyPackage \[ \]* \[out\]
</dt> <dd>

Tipo: **uint8**

Secuencia de bytes que contiene la clave de cifrado de un volumen, protegida por el protector de clave especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                            | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>           | El volumen está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ NO \_ SE \_ ENCONTRÓ \_ EL**</dt> <dt>PROTECTOR 2150694963 (0x80310033)</dt> </dl>    | El protector de clave proporcionado no existe en el volumen.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ TIPO DE PROTECTOR \_ \_ NO**</dt> <dt>VÁLIDO 2150694970 (0x8031003A)</dt> </dl> | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "Contraseña numérica" o "Clave externa". Use el [**método ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para crear un protector de clave del tipo adecuado.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
