---
description: Enumera los protectores usados para proteger la clave de cifrado del volumen.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Método GetKeyProtectors de la Win32_EncryptableVolume clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270764"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectors de la clase EncryptableVolume de Win32 \_

El **método GetKeyProtectors** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) enumera los protectores usados para proteger la clave de cifrado del volumen. Si se proporciona un tipo de protector, solo se devuelven los protectores de clave de volumen del tipo especificado.

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

Tipo: **uint32**

Entero sin signo que especifica el tipo de protector de clave que se devolverá.

Si no se especifica este parámetro, se devuelven todos los protectores de clave disponibles del volumen.



| Value                                                                         | Significado                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Todos los tipos.<br/> Se devuelven todos los protectores de clave.<br/> |
| <dl> <dt>1</dt> </dl>  | Módulo de plataforma segura (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Clave externa.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Contraseña numérica.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM y PIN.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM y clave de inicio.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM y PIN y clave de inicio.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Clave pública.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Contraseña.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | Certificado de TPM<br/>                                        |
| <dl> <dt>10</dt> </dl> | Identificador de seguridad (SID)<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz de cadenas que identifican los protectores de clave usados para proteger la clave de cifrado del volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Se *especifica el parámetro VolumeKeyProtectorID,* pero no hace referencia a un *keyProtectorType válido.*<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                   |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
