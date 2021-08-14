---
description: El objeto Divider usa recognizerContext para mejorar su análisis de segmentos de reconocimiento y generar texto de reconocimiento para los elementos de escritura a mano.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Trabajar con un contexto de reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d99020e97170f0b68b1459abdc4b85f81ebc3fbba426233c2c13b5e042f28ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715103"
---
# <a name="working-with-a-recognizer-context"></a>Trabajar con un contexto de reconocedor

El [**objeto Divider**](inkdivider-class.md) usa [**recognizerContext para**](inkrecognizercontext-class.md) mejorar su análisis de segmentos de reconocimiento y generar texto de reconocimiento para los elementos de escritura a mano.

Puede establecer el contexto del reconocedor mediante la propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) del objeto [**Divider**](inkdivider-class.md) o suministrando el contexto del reconocedor en la llamada al constructor [Divider](/previous-versions/ms839465(v=msdn.10)) (en código administrado). Si se asigna un contexto de reconocedor para un reconocedor que no es de escritura a mano o para un reconocedor que no admite la funcionalidad de entrada libre a la propiedad **RecognizerContext,** se produce una excepción.

Si los reconocedores no están instalados o no se asigna un contexto de reconocedor al objeto [**Divider,**](inkdivider-class.md) el objeto **Divider** no usa un contexto de reconocedor. En este caso, la característica de análisis de diseño realiza la división de segmentos y no hay texto asociado al [**objeto DivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)

> [!Note]  
> No se puede cambiar la propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) después de asignar trazos al [**objeto Divider.**](inkdivider-class.md) El **objeto Divider** usa los valores de propiedad predeterminados del [**objeto RecognizerContext.**](inkrecognizercontext-class.md)

 

El [**objeto Divider**](inkdivider-class.md) aplica el contexto del reconocedor a los elementos manuscritos durante el análisis de diseño. El objeto **Divider** omite todos los trazos que asigne directamente al contexto del reconocedor. Para obtener más información sobre el reconocimiento de texto, vea [Acerca del reconocimiento de escritura a mano.](about-handwriting-recognition.md)

 

 
