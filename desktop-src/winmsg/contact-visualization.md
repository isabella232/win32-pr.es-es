---
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta un contacto de entrada.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualización de contactos (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361237"
---
# <a name="contact-visualization"></a>Visualización de contactos

Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta un contacto de entrada.

Estas constantes se utilizan con los parámetros **SPI \_ GETCONTACTVISUALIZATION** y **SPI \_ SETCONTACTVISUALIZATION** y la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ desactivado**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica la información de la interfaz de usuario para todos los contactos está desactivada.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica la información de la interfaz de usuario para todos los contactos está activada.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ PRESENTATIONMODE**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica la información de la interfaz de usuario para todos los contactos está activada con los objetos visuales de modo de presentación.


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

[**Visualización de gestos**](gesture-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuración de comentarios de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

