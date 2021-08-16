---
description: Evento que tiene lugar cuando se conecta un nuevo Windows de hardware de adquisición de imágenes (WIA).
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento Wia.OnDeviceConnected
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
ms.openlocfilehash: d878cc663cc9f7ea1422e2dc2cad10e652296a48ef597cf699fe5eb3af99e49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209552"
---
# <a name="wiaondeviceconnected-event"></a>Evento Wia.OnDeviceConnected

Evento que tiene lugar cuando se conecta un nuevo Windows de hardware de adquisición de imágenes (WIA).

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

## <a name="remarks"></a>Comentarios

WIA notifica al script o a la aplicación cada vez que se conecta un nuevo dispositivo de hardware al equipo. Implemente **la subrutina objWia** \_ **OnDeviceConnected()** para permitir que el script o la aplicación respondan a la conexión del dispositivo.

Por ejemplo, es posible que desee que un script actualice la colección [**Dispositivos**](-wia-iwia-devices.md) cuando se instala un nuevo dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




