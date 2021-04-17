---
description: Devuelve la clave externa de un archivo.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Método GetExternalKeyFromFile de la clase Win32_EncryptableVolume
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688163"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Método GetExternalKeyFromFile de la \_ clase EncryptableVolume de Win32

El método **GetExternalKeyFromFile** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve la clave externa de un archivo creado por [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), dada la ubicación de ese archivo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PathWithFileName* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena que especifica la ubicación del archivo que contiene una clave externa.

</dd> <dt>

*ExternalKey* \[ enuncia\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matriz de bytes que es la clave externa de 256 bits incluida en el archivo que se puede usar para desbloquear un volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                   | Descripción                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                   | Método realizado correctamente.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | El archivo no contiene una clave externa.<br/>  |
| <dl> <dt>**Error \_ de \_No \_ se encontró el archivo**</dt> <dt>2147942402 (0x80070002)</dt> </dl> | No se encuentra el archivo en la ubicación especificada.<br/> |



 

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

 

 
