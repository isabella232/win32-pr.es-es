---
description: Evento que tiene lugar cuando se desconecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento WIA. OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276866"
---
# <a name="wiaondevicedisconnected-event"></a>Evento WIA. OnDeviceDisconnected

Evento que tiene lugar cuando se desconecta un nuevo dispositivo de hardware de adquisición de imágenes de Windows (WIA).

## <a name="syntax"></a>Sintaxis


```JScript
Wia.OnDeviceDisconnected(
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

WIA notifica al script o a la aplicación cada vez que un dispositivo de hardware se desconecta del equipo. Implemente la subrutina **objWia** \_ **OnDeviceDisconnected ()** para permitir que el script o la aplicación respondan a la desconexión del dispositivo.

Por ejemplo, puede que desee un script para actualizar la recopilación de [**dispositivos**](-wia-iwia-devices.md) cuando se quita un dispositivo del equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




