---
description: Evento que tiene lugar cuando se conecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276867"
---
# <a name="wiaondeviceconnected-event"></a>Evento WIA. OnDeviceConnected

Evento que tiene lugar cuando se conecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).

## <a name="syntax"></a>Sintaxis


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Cadena que contiene el identificador del dispositivo conectado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

WIA notifica al script o a la aplicación cada vez que se conecta un nuevo dispositivo de hardware al equipo. Implemente la \_ subrutina objWia **OnDeviceConnected ()** para permitir que el script o la aplicación respondan a la conexión del dispositivo.

Por ejemplo, puede que desee un script para actualizar la recopilación de [**dispositivos**](-wia-iwia-devices.md) cuando se instala un nuevo dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




