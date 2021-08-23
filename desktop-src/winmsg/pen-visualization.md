---
description: Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos de lápiz enumerados.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualización de lápiz (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60b9f75493a361cc167b65fba1783bc01f909d76211b1076e2faccc2e6f00116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548495"
---
# <a name="pen-visualization"></a>Visualización de lápiz

Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos de lápiz enumerados.

Estas constantes se usan con los parámetros **SPI \_ GETPENVISUALIZATION** y **SPI \_ SETPENVISUALIZATION** y la [**función SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que los comentarios de la interfaz de usuario para todos los gestos de lápiz están desactivados.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Especifica que los comentarios de la interfaz de usuario para todos los gestos de lápiz están en .


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PULSACIÓN DE \_ PENVISUALIZACIÓN**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para una pulsación de lápiz.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para una doble pulsación de lápiz.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION \_ CURSOR**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para el cursor de lápiz.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                 |
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

 

