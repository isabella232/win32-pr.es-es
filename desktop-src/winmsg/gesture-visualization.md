---
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos de la lista.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualización de gestos (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697601"
---
# <a name="gesture-visualization"></a>Visualización de gestos

Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos de la lista.

Estas constantes se utilizan con los parámetros **SPI \_ GETGESTUREVISUALIZATION** y **SPI \_ SETGESTUREVISUALIZATION** y la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**Note**  

Para recuperar o establecer la información de visualización del lápiz, se recomienda usar los parámetros **SPI \_ GETPENVISUALIZATION** y **SPI \_ SETPENVISUALIZATION** y las constantes enumeradas en la [**visualización del lápiz**](pen-visualization.md).

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ desactivado**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que los comentarios de la interfaz de usuario para todos los gestos están desactivados.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Especifica que la información de la interfaz de usuario para todos los gestos está activada.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION \_ TAP**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica la información de la interfaz de usuario para una derivación.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica la información de la interfaz de usuario para una doble punteo.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Especifica la información de la interfaz de usuario para presionar y pulsar.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Especifica la información de la interfaz de usuario para mantener presionado.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Especifica la información de la interfaz de usuario para una derivación derecha.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de configuración](configuration-constants.md)
</dt> <dt>

[**Visualización de contactos**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuración de comentarios de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

