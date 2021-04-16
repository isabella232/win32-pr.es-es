---
description: Enumera los protectores usados para proteger la clave de cifrado del volumen.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Método GetKeyProtectors de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686649"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectors de la \_ clase EncryptableVolume de Win32

El método **GetKeyProtectors** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) enumera los protectores usados para proteger la clave de cifrado del volumen. Si se proporciona un tipo de protector, solo se devuelven los protectores de clave de volumen del tipo especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*KeyProtectorType* \[ en, opcional\]
</dt> <dd>

Tipo: **UInt32**

Entero sin signo que especifica el tipo de protector de clave que se va a devolver.

Si no se especifica este parámetro, se devuelven todos los protectores de clave disponibles del volumen.



| Value                                                                         | Significado                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Todos los tipos.<br/> Se devuelven todos los protectores de clave.<br/> |
| <dl> <dt>1</dt> </dl>  | Módulo de plataforma segura (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Clave externa.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Contraseña numérica.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM y PIN.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM y clave de inicio.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM y clave de inicio y PIN.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Clave pública.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Frase.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | Certificado TPM<br/>                                        |
| <dl> <dt>10</dt> </dl> | Identificador de seguridad (SID)<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String \[ \]**

Matriz de cadenas que identifican los protectores de clave usados para proteger la clave de cifrado del volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Se ha especificado el parámetro *VolumeKeyProtectorID* pero no hace referencia a un *KeyProtectorType* válido.<br/> |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                   |



 

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

 

 
