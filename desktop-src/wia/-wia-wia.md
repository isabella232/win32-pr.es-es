---
description: El objeto Wia es el punto de entrada de todas las Windows de scripting de adquisición de imágenes (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Objeto Wia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 38dc5f7ac4440320827e009a7fd38dd6554ceb70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574393"
---
# <a name="wia-object"></a>Objeto Wia

El **objeto Wia** es el punto de entrada de todas las Windows de scripting de adquisición de imágenes (WIA). Cualquier aplicación que use el modelo de scripting de WIA debe crear un [**objeto SafeWia**](-wia-safewia.md) **o Wia.** Use ese objeto para enumerar y crear dispositivos y para recibir notificaciones de eventos de hardware.

> [!Note]  
> Este objeto no es seguro para scripting. Para obtener una versión de este objeto que sea segura para scripting, vea [**SafeWia**](-wia-safewia.md).

 

## <a name="members"></a>Members

El **objeto Wia** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

El **objeto Wia** tiene estos eventos.



| Evento                                                                 | Descripción                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Evento que tiene lugar cuando se conecta un nuevo dispositivo de hardware WIA.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Evento que tiene lugar cuando se desconecta un nuevo dispositivo de hardware WIA.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Evento que tiene lugar cuando una transferencia de datos se completa correctamente.<br/> |



 

### <a name="methods"></a>Métodos

El **objeto Wia** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Crear**](-wia-iwia-create.md) | El [**método Create**](-wia-iwia-create.md) del objeto **Wia** establece una conexión con el dispositivo WIA especificado y devuelve un objeto [**Item**](-wia-item.md) que representa el dispositivo.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto Wia** tiene estas propiedades.




| Propiedad | Tipo de acceso | Descripción | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br /> | Solo lectura<br /> | Colección de <a href="-wia-deviceinfo.md"><strong>objetos DeviceInfo</strong></a> que representa todos los dispositivos instalados en el equipo. Solo lectura. <br /><blockquote>[!Note]<br />Esta colección está basada en 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |
| IID<br/>                      | CLSID \_ Wia<br/>                                                                                         |



 

 




