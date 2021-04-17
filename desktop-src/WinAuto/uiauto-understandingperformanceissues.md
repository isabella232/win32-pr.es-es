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
# <a name="understanding-performance-issues"></a>Descripción de los problemas de rendimiento

En este tema se describen los problemas de rendimiento asociados al uso de los patrones de control [Text y TextRange](uiauto-implementingtextandtextrange.md) .


Las interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) y [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) dependen de llamadas entre procesos; no proporcionan un mecanismo de almacenamiento en caché para mejorar el rendimiento al recuperar o procesar contenido textual.

Una aplicación cliente puede mejorar el rendimiento mediante el método [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar bloques de texto de tamaño moderado. Por ejemplo, el uso de **gettext** para recuperar caracteres individuales incurrirá en un impacto de rendimiento entre procesos para cada carácter, mientras que si no se especifica una longitud máxima al llamar a **gettext** , se producirá un acierto entre procesos, pero puede tener una latencia elevada según el tamaño del intervalo de texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




