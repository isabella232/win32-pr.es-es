---
description: Recupera el número de veces que se ha suspendido BitLocker.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Método GetSuspendCount de la clase Win32_EncryptableVolume (Activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688151"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Método GetSuspendCount de la \_ clase EncryptableVolume de Win32

El método **GetSuspendCount** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera el número de reinicios antes de que se reanude la protección.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SuspendCount* 
</dt> <dd>

Valor entero comprendido entre 0 y 15.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código devuelto                                                                                          | Descripción                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                 | Método realizado correctamente.<br/>                                      |
| <dl> <dt>**ERROR \_ no \_ admitido**</dt> </dl> | Se devuelve si el volumen no está suspendido o no es un volumen del sistema operativo.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método solo se aplica al volumen del sistema operativo y solo si realmente se suspende en ese momento. Si el volumen no está suspendido o no es un volumen del sistema operativo, se devolverá un **error \_ no \_ admitido** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| Encabezado<br/>                   | <dl> <dt>Activdbg. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




