---
description: Escribe la clave externa asociada al protector de clave de volumen especificado en un archivo de solo lectura oculto del sistema en la carpeta especificada.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Método SaveExternalKeyToFile de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 02269d2b2339ebc8a2b6022bc5f02e63710d496e768be09dad9993c177ed5de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004293"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Método SaveExternalKeyToFile de la clase EncryptableVolume de Win32 \_

El **método SaveExternalKeyToFile** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) escribe la clave externa asociada al protector de clave de volumen especificado en un archivo de solo lectura oculto del sistema en la carpeta especificada.

Este método solo es aplicable a los protectores de clave del tipo "Clave externa" o "TPM y clave de inicio".

## <a name="syntax"></a>Sintaxis


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado.

</dd> <dt>

*Ruta de acceso* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que contiene la ubicación del volumen o la carpeta donde se guardará la clave externa asociada al protector de clave especificado. Esta ruta de acceso no incluye el nombre del archivo, que es interno y puede cambiar de versión a versión. Use **GetExternalKeyFileName para** obtener el nombre de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                   | Método realizado correctamente.<br/>                                                                                                             |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME 2150694912**</dt> <dt>(0x80310000)</dt> </dl>  | El volumen está bloqueado.<br/>                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | El *parámetro VolumeKeyProtectorID* no hace referencia a un protector de clave del tipo "Clave externa" o "TPM y clave de inicio".<br/>            |
| <dl> <dt>**ERROR \_ RUTA \_ DE \_ ACCESO NO**</dt> 2147942403 <dt>(0x80070003)</dt> </dl> | El *parámetro Path* no hace referencia a una ubicación válida.<br/> Asegúrese de que el nombre de archivo no está incluido en el *parámetro Path.*<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                      |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, solo Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
