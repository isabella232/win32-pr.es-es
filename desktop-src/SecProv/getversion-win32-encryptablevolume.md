---
description: Devuelve la versión de metadatos de FVE del volumen.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Método GetVersion de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 0681498a0d075fa22bada520e22c0ae626a4764d1a917f7090b796f05d66b122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891906"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>Método GetVersion de la clase EncryptableVolume de Win32 \_

El **método GetVersion** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve la versión de metadatos de FVE del volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Versión* \[ out\]
</dt> <dd>

Tipo: **uint32**

Entero sin signo que indica la versión de metadatos del volumen.



| Valor                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl> | Se desconoce el sistema operativo.<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Windows Formato vista, lo que significa que el volumen se protegió con BitLocker en un equipo que ejecuta Windows Vista.<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Windows formato 7, lo que significa que el volumen se protegió con BitLocker en un equipo que ejecuta Windows 7 o que el formato de metadatos se actualizó mediante el método [**UpgradeVolume.**](upgradevolume-win32-encryptablevolume.md)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Si el volumen ya está desbloqueado y no se producen otros errores, este método devuelve cero.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                       | El método se ha llevado a cabo de forma correcta.<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl> | El valor del *parámetro Version* no es válido.<br/> |
| <dl> <dt>**ERROR \_ DATOS \_ NO VÁLIDOS**</dt> <dt>13 (0xD)</dt> </dl>       | El controlador devolvió un formato de datos no admitido.<br/>     |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
