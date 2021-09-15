---
description: El objeto Divider usa recognizerContext para mejorar su análisis de segmentos de reconocimiento y generar texto de reconocimiento para los elementos de escritura a mano.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Trabajar con un contexto de reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467948"
---
# <a name="working-with-a-recognizer-context"></a>Trabajar con un contexto de reconocedor

El [**objeto Divider**](inkdivider-class.md) usa [**recognizerContext para**](inkrecognizercontext-class.md) mejorar su análisis de segmentos de reconocimiento y generar texto de reconocimiento para los elementos de escritura a mano.

Puede establecer el contexto del reconocedor mediante la propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) del objeto [**Divider**](inkdivider-class.md) o si proporciona el contexto del reconocedor en la llamada al constructor [Divider](/previous-versions/ms839465(v=msdn.10)) (en código administrado). Si se asigna un contexto de reconocedor para un reconocedor que no es de escritura a mano o para un reconocedor que no admite la funcionalidad de entrada libre a la propiedad **RecognizerContext,** se produce una excepción.

Si los reconocedores no están instalados o no se asigna un contexto de reconocedor al objeto [**Divider,**](inkdivider-class.md) el objeto **Divider** no usa un contexto de reconocedor. En este caso, la característica de análisis de diseño realiza la división de segmentos y no hay texto asociado al [**objeto DivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)

> [!Note]  
> La [**propiedad RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) no se puede cambiar después de que se hayan asignado trazos al [**objeto Divider.**](inkdivider-class.md) El **objeto Divider** usa los valores de propiedad predeterminados del [**objeto RecognizerContext.**](inkrecognizercontext-class.md)

 

El [**objeto Divider**](inkdivider-class.md) aplica el contexto del reconocedor a los elementos manuscritos durante el análisis de diseño. El objeto **Divider** omite los trazos que asigne directamente al contexto del reconocedor. Para obtener más información sobre el reconocimiento de texto, vea [Acerca del reconocimiento de escritura a mano.](about-handwriting-recognition.md)

 

 
