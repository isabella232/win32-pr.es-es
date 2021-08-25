---
description: El objeto DeviceInfo proporciona acceso a las propiedades de un Windows de hardware de adquisición de imágenes (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Objeto DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 69b34a97483a8a6ce231890454148c7948f63e4e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467182"
---
# <a name="deviceinfo-object"></a>Objeto DeviceInfo

El **objeto DeviceInfo** proporciona acceso a las propiedades de un Windows de hardware de adquisición de imágenes (WIA). También, a través de su [**método Create,**](-wia-iwiadeviceinfo-create.md) proporciona una manera de que la aplicación o el script se conecten al dispositivo y obtengan un objeto [**Item**](-wia-item.md) que represente el dispositivo. Use el [**método Devices**](-wia-iwia-devices.md) para obtener una colección de **objetos DeviceInfo.**

## <a name="members"></a>Miembros

El **objeto DeviceInfo** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto DeviceInfo** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Crear**](-wia-iwiadeviceinfo-create.md)           | El [**método Create**](-wia-iwiadeviceinfo-create.md) del objeto **DeviceInfo** establece una conexión con el dispositivo WIA especificado por el **objeto DeviceInfo** y devuelve un objeto [**Item**](-wia-item.md) que representa el dispositivo.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | El [**método GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) del **objeto DeviceInfo** usa el identificador de una propiedad de dispositivo para devolver su valor.<br/>                                                                                               |



 

### <a name="properties"></a>Propiedades

El **objeto DeviceInfo** tiene estas propiedades.




| Propiedad | Tipo de acceso | Descripción | 
|----------|-------------|-------------|
| <a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a><br /> | Solo lectura<br /> | Recupera el identificador del dispositivo de hardware WIA. <br /> | 
| <a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Fabricante</strong></a><br /> | Solo lectura<br /> | Recupera el nombre del fabricante de este dispositivo de hardware.<br /> | 
| <a href="-wia-iwiadeviceinfo-name.md"><strong>Nombre</strong></a><br /> | Solo lectura<br /> | Nombre del dispositivo de hardware WIA tal como aparece en la interfaz de usuario.<br /> | 
| <a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a><br /> | Solo lectura<br /> | Recupera el puerto al que está conectado el dispositivo de hardware WIA.<br /> | 
| <a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a><br /> | Solo lectura<br /> | Recupera el tipo de dispositivo de hardware WIA. Los valores posibles son: <br /><ul><li>DigitalCamera</li><li>Escáner</li><li>StreamingVideo</li><li>Valor predeterminado</li></ul> | 
| <a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br /> | Solo lectura<br /> | Recupera el identificador de clase de la interfaz de usuario proporcionada por el fabricante para este dispositivo de hardware WIA. El valor es una representación de cadena de un GUID. <br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




