---
description: Información general sobre el marco de trabajo de servicios de texto para Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Marco de trabajo de servicios de texto (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688604"
---
# <a name="text-services-framework-tablet-pc"></a>Marco de trabajo de servicios de texto (Tablet PC)

Cuando el [marco de trabajo de servicios de texto (TSF)](../tsf/text-services-framework.md) está habilitado en un control con un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) asociado, el objeto PenInputPanel puede insertar texto directamente. Si el control no admite el marco de trabajo de servicios de texto (TSF), el objeto PenInputPanel debe recurrir al uso de la [función SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) para insertar texto.

La capacidad de insertar texto directamente es muy importante para los caracteres de Asia oriental, donde el uso de la [función SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) puede producir caracteres incorrectos.

TSF proporciona una interfaz para corregir errores de reconocimiento que permiten al usuario final corregir, reescribir o incluso dictar el texto adecuado.

TSF se habilita llamando al método [EnableTsf](/previous-versions/ms569656(v=vs.100)) con el parámetro *enable* establecido en **true**.

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



Un objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) asociado a un control [InkEdit](/previous-versions/ms552265(v=vs.100)) proporciona una experiencia de usuario sólida porque InkEdit admite TSF. Sin embargo, asegúrese de establecer la propiedad [InkMode](/previous-versions/ms835850(v=msdn.10)) en [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) en el control InkEdit, como se mencionó en el tema de [procedimientos](best-practices.md) recomendados.

En el [ejemplo PenInputPanel](peninputpanel-sample.md) se ofrece un ejemplo de cómo habilitar TSF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Text Services Framework (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 
