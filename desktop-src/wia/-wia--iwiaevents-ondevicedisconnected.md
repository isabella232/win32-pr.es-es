---
description: Evento que tiene lugar cuando se desconecta Windows dispositivo de hardware de adquisición de imágenes (WIA).
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento Wia.OnDeviceDisconnected
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
ms.openlocfilehash: b9d61d196e3a9a7471b9a1fb1ab86c3ba918427ccc5dd5060ffaabdf28f80871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442161"
---
# <a name="wiaondevicedisconnected-event"></a>Evento Wia.OnDeviceDisconnected

Evento que tiene lugar cuando se desconecta Windows dispositivo de hardware de adquisición de imágenes (WIA).

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

WIA notifica al script o a la aplicación cada vez que se desconecta un dispositivo de hardware del equipo. Implemente la subrutina **objWia** \_ **OnDeviceDisconnected()** para permitir que el script o la aplicación respondan a la desconexión del dispositivo.

Por ejemplo, es posible que desee que un script actualice la [**colección Dispositivos**](-wia-iwia-devices.md) cuando se quita un dispositivo del equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




