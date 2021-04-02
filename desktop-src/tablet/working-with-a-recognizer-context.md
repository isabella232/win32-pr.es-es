---
description: El objeto divisor utiliza un objeto RecognizerContext para mejorar su análisis de segmentos de reconocimiento y para generar texto de reconocimiento para los elementos de escritura a mano.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Trabajar con un contexto de reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082199"
---
# <a name="working-with-a-recognizer-context"></a>Trabajar con un contexto de reconocedor

El objeto [**divisor**](inkdivider-class.md) utiliza un objeto [**RecognizerContext**](inkrecognizercontext-class.md) para mejorar su análisis de segmentos de reconocimiento y para generar texto de reconocimiento para los elementos de escritura a mano.

Puede establecer el contexto del reconocedor mediante la propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) del objeto [**divisor**](inkdivider-class.md) o proporcionando el contexto del reconocedor en la llamada al constructor de [divisor](/previous-versions/ms839465(v=msdn.10)) (en código administrado). Si un contexto de reconocedor para un reconocedor que no es de escritura a mano o para un reconocedor que no admite la función de entrada libre se asigna a la propiedad **RecognizerContext** , se produce una excepción.

Si no se instalan los reconocedores o si no se asigna un contexto de reconocedor al objeto [**divisor**](inkdivider-class.md) , el objeto de **divisor** no utiliza un contexto de reconocedor. En este caso, la característica de análisis de diseño realiza la división del segmento y no hay texto asociado al objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

> [!Note]  
> No se puede cambiar la propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) una vez que se han asignado trazos al objeto [**divisor**](inkdivider-class.md) . El objeto **divisor** utiliza los valores de propiedad predeterminados del objeto [**RecognizerContext**](inkrecognizercontext-class.md) .

 

El objeto [**divisor**](inkdivider-class.md) aplica el contexto del reconocedor a los elementos escritos a mano durante el análisis del diseño. El objeto **divisor** omite cualquier trazo que se asigne directamente al contexto del reconocedor. Para obtener más información sobre el reconocimiento de texto, consulte [acerca del reconocimiento de escritura a mano](about-handwriting-recognition.md).

 

 
