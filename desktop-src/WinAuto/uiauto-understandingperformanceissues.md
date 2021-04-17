---
title: Descripción de los problemas de rendimiento
description: En este tema se describen los problemas de rendimiento asociados al uso de los patrones de control Text y TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- clientes, descripción de los problemas de rendimiento
- clientes, controles basados en texto
- clientes, intervalos de texto
- clients, patrón de control Text
- clients, patrón de control TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359537"
---
# <a name="understanding-performance-issues"></a><span data-ttu-id="e9802-108">Descripción de los problemas de rendimiento</span><span class="sxs-lookup"><span data-stu-id="e9802-108">Understanding Performance Issues</span></span>

<span data-ttu-id="e9802-109">En este tema se describen los problemas de rendimiento asociados al uso de los patrones de control [Text y TextRange](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="e9802-109">This topic describes performance issues associated with using the [Text and TextRange](uiauto-implementingtextandtextrange.md) control patterns.</span></span>


<span data-ttu-id="e9802-110">Las interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) y [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) dependen de llamadas entre procesos; no proporcionan un mecanismo de almacenamiento en caché para mejorar el rendimiento al recuperar o procesar contenido textual.</span><span class="sxs-lookup"><span data-stu-id="e9802-110">The [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces rely on cross-process calls—they do not provide a caching mechanism to improve performance when retrieving or processing textual content.</span></span>

<span data-ttu-id="e9802-111">Una aplicación cliente puede mejorar el rendimiento mediante el método [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar bloques de texto de tamaño moderado.</span><span class="sxs-lookup"><span data-stu-id="e9802-111">A client application can improve performance by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method to retrieve moderately sized blocks of text.</span></span> <span data-ttu-id="e9802-112">Por ejemplo, el uso de **gettext** para recuperar caracteres individuales incurrirá en un impacto de rendimiento entre procesos para cada carácter, mientras que si no se especifica una longitud máxima al llamar a **gettext** , se producirá un acierto entre procesos, pero puede tener una latencia elevada según el tamaño del intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="e9802-112">For example, using **GetText** to retrieve single characters will incur a cross-process performance hit for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9802-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9802-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9802-114">Patrones de control Text y TextRange</span><span class="sxs-lookup"><span data-stu-id="e9802-114">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="e9802-115">Compatibilidad de UI Automation para el contenido textual</span><span class="sxs-lookup"><span data-stu-id="e9802-115">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="e9802-116">Trabajar con controles basados en texto</span><span class="sxs-lookup"><span data-stu-id="e9802-116">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




