---
description: El objeto SafeWia es un \# punto de entrada &0034; Safe para scripting&\# 0034; para todas las funciones de scripting de adquisición de imágenes de Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Objeto SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715184"
---
# <a name="safewia-object"></a>Objeto SafeWia

El objeto **SafeWia** es un punto de entrada "Safe for scripting" para todas las funciones de scripting de adquisición de imágenes de Windows (WIA). Cualquier aplicación que use el modelo de scripting de WIA debe crear un objeto **SafeWia** o [**WIA**](-wia-wia.md) . Use ese objeto para enumerar y crear dispositivos y recibir notificaciones de eventos de hardware.

## <a name="members"></a>Miembros

El objeto **SafeWia** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SafeWia** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**A**](-wia-iwia-create.md) | El método [**Create**](-wia-iwia-create.md) del objeto [**WIA**](-wia-wia.md) establece una conexión con el dispositivo WIA especificado y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SafeWia** tiene estas propiedades.



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
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Colección de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos los dispositivos instalados en el equipo. Solo lectura. <br/>
<blockquote>
[!Note]<br />
Esta colección está basada en 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WIA**](-wia-wia.md)
</dt> </dl>

 

 




