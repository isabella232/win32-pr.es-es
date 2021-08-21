---
description: Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos enumerados.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualización de gestos (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f572addf2ad7a98dbe3afc63c69a305ea15546e9533918d952271372cf52b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849824"
---
# <a name="gesture-visualization"></a>Visualización de gestos

Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos enumerados.

Estas constantes se usan con los parámetros **SPI \_ GETGESTUREVISUALIZATION** y **SPI \_ SETGESTUREVISUALIZATION** y la [**función SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

**Nota**  

Para recuperar o establecer la información de visualización del lápiz, se recomienda usar los parámetros **SPI \_ GETPENVISUALIZATION** y **SPI \_ SETPENVISUALIZATION** y las constantes enumeradas en [**Visualización**](pen-visualization.md)de lápiz .

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que los comentarios de la interfaz de usuario para todos los gestos están desactivados.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Especifica que los comentarios de la interfaz de usuario para todos los gestos están en .


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTOVISUALIZACIÓN \_ TAP**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para una pulsación.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para una doble pulsación.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para presionar y pulsar.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para mantener presionado.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTOVISUALIZACIÓN \_ RIGHTTAP**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para pulsar a la derecha.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



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

 

