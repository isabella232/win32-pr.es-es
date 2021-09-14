---
description: Devuelve la clave externa de un archivo.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Método GetExternalKeyFromFile de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243986"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Método GetExternalKeyFromFile de la clase EncryptableVolume de Win32 \_

El **método GetExternalKeyFromFile** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve la clave externa de un archivo creado por [**SaveExternalKeyToFile,**](saveexternalkeytofile-win32-encryptablevolume.md)dada la ubicación de ese archivo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PathWithFileName* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la ubicación del archivo que contiene una clave externa.

</dd> <dt>

*ExternalKey* \[ out\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matriz de bytes que es la clave externa de 256 bits contenida en el archivo que se puede usar para desbloquear un volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                   | Método realizado correctamente.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | El archivo no contiene una clave externa.<br/>  |
| <dl> <dt>**ERROR \_ ARCHIVO \_ NO \_ ENCONTRADO**</dt> <dt>2147942402 (0x80070002)</dt> </dl> | No se encuentra el archivo en la ubicación especificada.<br/> |



 

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
