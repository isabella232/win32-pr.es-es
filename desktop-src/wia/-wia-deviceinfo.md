---
description: El objeto DeviceInfo proporciona acceso a las propiedades de un dispositivo de hardware de adquisición de imágenes de Windows (WIA).
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
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659885"
---
# <a name="deviceinfo-object"></a>Objeto DeviceInfo

El objeto **DeviceInfo** proporciona acceso a las propiedades de un dispositivo de hardware de adquisición de imágenes de Windows (WIA). También, a través de su método [**Create**](-wia-iwiadeviceinfo-create.md) , proporciona una forma para que la aplicación o el script se conecten al dispositivo y obtengan un objeto de [**elemento**](-wia-item.md) que represente el dispositivo. Use el método [**Devices**](-wia-iwia-devices.md) para obtener una colección de objetos **DeviceInfo** .

## <a name="members"></a>Miembros

El objeto **DeviceInfo** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **DeviceInfo** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**A**](-wia-iwiadeviceinfo-create.md)           | El método [**Create**](-wia-iwiadeviceinfo-create.md) del objeto **DeviceInfo** establece una conexión con el dispositivo WIA especificado por el objeto **DeviceInfo** y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | El método [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) del objeto **DEVICEINFO** usa el identificador de una propiedad de dispositivo para devolver su valor.<br/>                                                                                               |



 

### <a name="properties"></a>Propiedades

El objeto **DeviceInfo** tiene estas propiedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propiedad</th>
<th style="text-align: left;">Tipo de acceso</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-id.md"><strong>Sesión</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Recupera el identificador del dispositivo de hardware WIA. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Le</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Recupera el nombre del fabricante de este dispositivo de hardware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">El nombre del dispositivo de hardware WIA tal como aparece en la interfaz de usuario.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Recupera el puerto al que está conectado el dispositivo de hardware WIA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Recupera el tipo de dispositivo de hardware WIA. Los valores posibles son: <br/>
<ul>
<li>DigitalCamera</li>
<li>Escáner</li>
<li>StreamingVideo</li>
<li>Valor predeterminado</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Recupera el ID. de clase de la interfaz de usuario proporcionada por el fabricante para este dispositivo de hardware WIA. El valor es una representación de cadena de un GUID. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




