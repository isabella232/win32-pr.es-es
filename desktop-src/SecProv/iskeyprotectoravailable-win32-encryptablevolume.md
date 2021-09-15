---
description: Indica si hay protectores disponibles para el volumen.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Método IsKeyProtectorAvailable de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270668"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a>Método IsKeyProtectorAvailable de la clase EncryptableVolume de Win32 \_

El **método IsKeyProtectorAvailable** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si hay protectores disponibles para el volumen.

Si se proporciona un tipo de protector, el método indica si los protectores del tipo especificado están disponibles para el volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*KeyProtectorType* \[ en, opcional\]
</dt> <dd>

Tipo: **uint32**

Entero sin signo que indica el tipo de protector de clave de volumen que se ha consultado.

Si no se especifica este parámetro, se consultan todos los protectores de clave disponibles del volumen.



| Value                                                                         | Significado                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Todos los tipos.<br/> Se consultan todos los protectores de clave.<br/> |
| <dl> <dt>1</dt> </dl>  | Módulo de plataforma segura (TPM).<br/>                        |
| <dl> <dt>2</dt> </dl>  | Clave externa.<br/>                                         |
| <dl> <dt>3</dt> </dl>  | Contraseña numérica.<br/>                                   |
| <dl> <dt>4</dt> </dl>  | TPM y PIN.<br/>                                          |
| <dl> <dt>5</dt> </dl>  | TPM y clave de inicio.<br/>                                  |
| <dl> <dt>6</dt> </dl>  | TPM y PIN y clave de inicio.<br/>                          |
| <dl> <dt>7</dt> </dl>  | Clave pública.<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Contraseña.<br/>                                           |
| <dl> <dt>9</dt> </dl>  | Certificado de TPM<br/>                                       |
| <dl> <dt>10</dt> </dl> | Identificador de seguridad (SID)<br/>                             |



 

</dd> <dt>

*IsKeyProtectorAvailable* \[ out\]
</dt> <dd>

Tipo: **booleano**

Valor booleano que indica si existe un protector de clave de volumen del tipo especificado en el volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                         | Descripción                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                         | Método realizado correctamente.<br/>                                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl> | Se *especifica el parámetro KeyProtectorType,* pero no hace referencia a un tipo de protector de clave válido.<br/> |



 

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

 

 
