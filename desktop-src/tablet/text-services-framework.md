---
description: Información general sobre el marco de servicios de texto para Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Text Services Framework (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467950"
---
# <a name="text-services-framework-tablet-pc"></a>Text Services Framework (Tablet PC)

Cuando el [Text Services Framework (TSF)](../tsf/text-services-framework.md) está habilitado en un control con un [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) asociado, el objeto PenInputPanel puede insertar texto directamente. Si el control no admite Text Services Framework (TSF), el objeto PenInputPanel debe recurrir al uso de la [función SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) para insertar texto.

La capacidad de insertar texto directamente es muy importante para aquellos que introducen caracteres asiáticos orientales, donde el uso de [la función SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) puede generar caracteres incorrectos.

TSF proporciona una interfaz para corregir los errores de reconocimiento, lo que permite al usuario final corregir, reescribir o incluso dictar el texto adecuado.

TSF se habilita mediante una llamada al [método EnableTsf](/previous-versions/ms569656(v=vs.100)) con el *parámetro enable* establecido en **TRUE.**

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



Un [objeto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) asociado a un control [InkEdit](/previous-versions/ms552265(v=vs.100)) proporciona una experiencia de usuario sólida porque InkEdit admite TSF. Sin embargo, asegúrese de establecer la [propiedad InkMode](/previous-versions/ms835850(v=msdn.10)) en [Microsoft.Ink.InkMode.Ink en](/previous-versions/ms827399(v=msdn.10)) el control InkEdit, como se mencionó en el [tema Procedimientos recomendados.](best-practices.md)

El [ejemplo PenInputPanel](peninputpanel-sample.md) proporciona un ejemplo de cómo habilitar TSF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Text Services Framework (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 
