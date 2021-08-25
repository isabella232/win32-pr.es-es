---
description: Recupera el número de veces que se ha suspendido BitLocker.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Método GetSuspendCount de la Win32_EncryptableVolume (Activdbg.h)
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
ms.openlocfilehash: 468bd6cdc8f3df7efba26997fd76b0724d3e4cc5da552275dad5201adc469f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906355"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Método GetSuspendCount de la clase EncryptableVolume de Win32 \_

El **método GetSuspendCount** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera el número de reinicios antes de que se reanude automáticamente la protección.

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

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código devuelto                                                                                          | Descripción                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Método realizado correctamente.<br/>                                      |
| <dl> <dt>**ERROR \_ NO \_ ADMITIDO**</dt> </dl> | Se devuelve si el volumen no está suspendido o no es un volumen del sistema operativo.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método solo se aplica al volumen del sistema operativo y solo si realmente se suspende en ese momento. Si el volumen no está suspendido o no es un volumen del sistema operativo, se devolverá **ERROR \_ NOT \_ SUPPORTED.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 Enterprise, Windows 8 Pro solo aplicaciones \[ de escritorio\]<br/>                                    |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| Header<br/>                   | <dl> <dt>Activdbg.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




