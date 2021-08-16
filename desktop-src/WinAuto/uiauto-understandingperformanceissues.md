---
title: Descripción de los problemas de rendimiento
description: En este tema se describen los problemas de rendimiento asociados con el uso de los patrones de control Text y TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- clientes, descripción de problemas de rendimiento
- clients,controles basados en texto
- clients,text ranges
- clients,Text control pattern
- clients,Patrón de control TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24846fea2f35cd9d265ab4f898b60dba2fc4e959b9a0f8bd7baea4661855f0a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861225"
---
# <a name="understanding-performance-issues"></a>Descripción de los problemas de rendimiento

En este tema se describen los problemas de rendimiento asociados con el uso de los patrones de control [Text y TextRange.](uiauto-implementingtextandtextrange.md)


Las interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) se basan en llamadas entre procesos, ya que no proporcionan un mecanismo de almacenamiento en caché para mejorar el rendimiento al recuperar o procesar contenido textual.

Una aplicación cliente puede mejorar el rendimiento mediante el método [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar bloques de texto de tamaño moderado. Por ejemplo, si se usa **GetText** para recuperar caracteres únicos, se generará un impacto en el rendimiento entre procesos de cada carácter, mientras que si no se especifica una longitud máxima al llamar a **GetText,** se generará un impacto entre procesos, pero puede tener una latencia alta en función del tamaño del intervalo de texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




