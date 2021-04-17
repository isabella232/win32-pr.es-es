---
description: Devuelve la versión de metadatos de FVE del volumen.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Método GetVersion de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686644"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>Método GetVersion de la \_ clase EncryptableVolume de Win32

El método **GetVersion** de la clase [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) devuelve la versión de metadatos de FVE del volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Versión* \[ de enuncia\]
</dt> <dd>

Tipo: **UInt32**

Entero sin signo que indica la versión de metadatos del volumen.



| Value                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl> | Se desconoce el sistema operativo.<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Formato de Windows Vista, lo que significa que el volumen se protegió con BitLocker en un equipo que ejecuta Windows Vista.<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Formato de Windows 7, lo que significa que el volumen se protegió con BitLocker en un equipo que ejecuta Windows 7 o que el formato de metadatos se actualizó mediante el método [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) .<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Si el volumen ya está desbloqueado y no se producen otros errores, este método devuelve cero.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl> | El valor del parámetro *version* no es válido.<br/> |
| <dl> <dt>**Error \_ de \_Datos no válidos**</dt> <dt>(0xd)</dt> </dl>       | El controlador devolvió un formato de datos no admitido.<br/>     |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
