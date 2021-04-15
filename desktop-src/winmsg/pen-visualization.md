---
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos del lápiz enumerados.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualización del lápiz (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545574"
---
# <a name="pen-visualization"></a>Visualización del lápiz

Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta uno de los gestos del lápiz enumerados.

Estas constantes se utilizan con los parámetros **SPI \_ GETPENVISUALIZATION** y **SPI \_ SETPENVISUALIZATION** y la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ desactivado**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que la información de la interfaz de usuario para todos los gestos de lápiz está desactivada.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Especifica que la información de la interfaz de usuario para todos los gestos de lápiz está activada.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION \_ TAP**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica la información de la interfaz de usuario para una TAP del lápiz.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica la información de la interfaz de usuario para una doble Punte de lápiz.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_cursor PENVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Especifica la información de la interfaz de usuario para el cursor del lápiz.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                 |
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

 

