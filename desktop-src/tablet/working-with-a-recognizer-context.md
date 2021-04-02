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
# <a name="working-with-a-recognizer-context"></a><span data-ttu-id="c948f-103">Trabajar con un contexto de reconocedor</span><span class="sxs-lookup"><span data-stu-id="c948f-103">Working with a Recognizer Context</span></span>

<span data-ttu-id="c948f-104">El objeto [**divisor**](inkdivider-class.md) utiliza un objeto [**RecognizerContext**](inkrecognizercontext-class.md) para mejorar su análisis de segmentos de reconocimiento y para generar texto de reconocimiento para los elementos de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="c948f-104">The [**Divider**](inkdivider-class.md) object uses a [**RecognizerContext**](inkrecognizercontext-class.md) to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span>

<span data-ttu-id="c948f-105">Puede establecer el contexto del reconocedor mediante la propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) del objeto [**divisor**](inkdivider-class.md) o proporcionando el contexto del reconocedor en la llamada al constructor de [divisor](/previous-versions/ms839465(v=msdn.10)) (en código administrado).</span><span class="sxs-lookup"><span data-stu-id="c948f-105">You can set the recognizer context by using the [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property of the [**Divider**](inkdivider-class.md) object or by supplying the recognizer context in the call to the [Divider](/previous-versions/ms839465(v=msdn.10)) constructor (in managed code).</span></span> <span data-ttu-id="c948f-106">Si un contexto de reconocedor para un reconocedor que no es de escritura a mano o para un reconocedor que no admite la función de entrada libre se asigna a la propiedad **RecognizerContext** , se produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="c948f-106">If a recognizer context for a non-handwriting recognizer or for a recognizer that does not support the free input capability is assigned to the **RecognizerContext** property, then an exception is thrown.</span></span>

<span data-ttu-id="c948f-107">Si no se instalan los reconocedores o si no se asigna un contexto de reconocedor al objeto [**divisor**](inkdivider-class.md) , el objeto de **divisor** no utiliza un contexto de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="c948f-107">If recognizers are not installed or a recognizer context is not assigned to the [**Divider**](inkdivider-class.md) object, the **Divider** object does not use a recognizer context.</span></span> <span data-ttu-id="c948f-108">En este caso, la característica de análisis de diseño realiza la división del segmento y no hay texto asociado al objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="c948f-108">In this case, the layout analysis feature performs the segment division, and no text is associated with the [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

> [!Note]  
> <span data-ttu-id="c948f-109">No se puede cambiar la propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) una vez que se han asignado trazos al objeto [**divisor**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c948f-109">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property cannot be changed after strokes have been assigned to the [**Divider**](inkdivider-class.md) object.</span></span> <span data-ttu-id="c948f-110">El objeto **divisor** utiliza los valores de propiedad predeterminados del objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c948f-110">The **Divider** object uses the default property values of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="c948f-111">El objeto [**divisor**](inkdivider-class.md) aplica el contexto del reconocedor a los elementos escritos a mano durante el análisis del diseño.</span><span class="sxs-lookup"><span data-stu-id="c948f-111">The [**Divider**](inkdivider-class.md) object applies the recognizer context to handwritten elements during layout analysis.</span></span> <span data-ttu-id="c948f-112">El objeto **divisor** omite cualquier trazo que se asigne directamente al contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="c948f-112">Any strokes you assign directly to the recognizer context are ignored by the **Divider** object.</span></span> <span data-ttu-id="c948f-113">Para obtener más información sobre el reconocimiento de texto, consulte [acerca del reconocimiento de escritura a mano](about-handwriting-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="c948f-113">For more information about text recognition, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

 

 
