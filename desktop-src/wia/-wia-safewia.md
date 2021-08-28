---
description: El objeto SafeWia es un &\# 0034;seguro para scripting&0034; punto de entrada para todas las funcionalidades de scripting de adquisición de imágenes de Windows \# (WIA).
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
ms.openlocfilehash: ef324934abee38e2581b6e05c0fdac92145e4f43
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473851"
---
# <a name="safewia-object"></a>Objeto SafeWia

El **objeto SafeWia** es un punto de entrada "seguro para scripting" para todas las Windows de scripting de adquisición de imágenes (WIA). Cualquier aplicación que use el modelo de scripting de WIA debe crear un **objeto SafeWia** [**o Wia.**](-wia-wia.md) Use ese objeto para enumerar y crear dispositivos y recibir notificaciones de eventos de hardware.

## <a name="members"></a>Miembros

El **objeto SafeWia** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SafeWia** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Crear**](-wia-iwia-create.md) | El [**método Create**](-wia-iwia-create.md) del objeto [**Wia**](-wia-wia.md) establece una conexión con el dispositivo WIA especificado y devuelve un objeto [**Item**](-wia-item.md) que representa el dispositivo.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SafeWia** tiene estas propiedades.




| Propiedad | Tipo de acceso | Descripción | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br /> | Solo lectura<br /> | Colección de <a href="-wia-deviceinfo.md"><strong>objetos DeviceInfo</strong></a> que representa todos los dispositivos instalados en el equipo. Solo lectura. <br /><blockquote>[!Note]<br />Esta colección está basada en 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Wia**](-wia-wia.md)
</dt> </dl>

 

 




