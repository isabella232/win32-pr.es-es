---
description: Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta un contacto de entrada.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualización de contactos (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea196017b1731bb176cd21a7dc02aaa360f4fe70503bd204b9c488d38eff99ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437258"
---
# <a name="contact-visualization"></a>Visualización de contactos

Las aplicaciones o marcos de interfaz de usuario usan las siguientes constantes para identificar cómo se procesan los comentarios de la interfaz de usuario cuando se detecta un contacto de entrada.

Estas constantes se usan con los parámetros **SPI \_ GETCONTACTVISUALIZATION** y **SPI \_ SETCONTACTVISUALIZATION** y la [**función SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que los comentarios de la interfaz de usuario para todos los contactos están desactivados.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para todos los contactos.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ PRESENTATIONMODE**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica los comentarios de la interfaz de usuario para todos los contactos con objetos visuales en modo de presentación.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de configuración](configuration-constants.md)
</dt> <dt>

[**Visualización de gestos**](gesture-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuración de comentarios de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

