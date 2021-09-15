---
title: Descripción de los problemas de rendimiento
description: En este tema se describen los problemas de rendimiento asociados al uso de los patrones de control Text y TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- clientes, descripción de problemas de rendimiento
- clientes, controles basados en texto
- clients,text ranges
- clients,Text control pattern
- clients,Patrón de control TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359228"
---
# <a name="understanding-performance-issues"></a>Descripción de los problemas de rendimiento

En este tema se describen los problemas de rendimiento asociados al uso de los patrones de control [Text y TextRange.](uiauto-implementingtextandtextrange.md)


Las interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) se basan en llamadas entre procesos: no proporcionan un mecanismo de almacenamiento en caché para mejorar el rendimiento al recuperar o procesar contenido textual.

Una aplicación cliente puede mejorar el rendimiento mediante el método [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar bloques de texto de tamaño moderado. Por ejemplo, si se usa **GetText** para recuperar caracteres únicos, se generará un impacto en el rendimiento entre procesos para cada carácter, mientras que si no se especifica una longitud máxima al llamar a **GetText,** se generará un impacto entre procesos, pero puede tener una latencia alta en función del tamaño del intervalo de texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




