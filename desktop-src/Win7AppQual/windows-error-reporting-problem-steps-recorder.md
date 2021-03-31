---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Informe de errores de Windows la grabadora de pasos del problema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818070"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Informe de errores de Windows la grabadora de pasos del problema

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  


## <a name="description"></a>Descripción

Antes de Windows 7, Informe de errores de Windows (WER) recopilaba informes de errores que indicaban problemas en la necesidad de reparación. Estos informes de errores contienen información útil que describe la naturaleza general de un problema, pero no hay información suficiente para determinar su causa principal. Para ello, los desarrolladores necesitan una herramienta para reproducir el escenario de bloqueo y bloqueo para la depuración.

Una nueva aplicación, la grabadora de pasos de problemas (PSR.exe), se envía a todas las compilaciones de Windows 7. Esta característica habilita la recopilación de las acciones realizadas por un usuario a la vez que encuentra un bloqueo para que los evaluadores y los desarrolladores puedan reproducir la situación de análisis y depuración.

## <a name="usage"></a>Uso

Actualmente, un desarrollador de servicios de Informe de errores de Windows debe solicitar la habilitación de los PSR para una aplicación; Las organizaciones de soporte técnico de Microsoft también usan esta herramienta mientras solucionan problemas con los usuarios finales. Los planes están en vigor para que PSR esté disponible en Windows Quality Online Services (WinQual) después del lanzamiento de Windows 7.

**Nota:** Con PSR habilitado para una aplicación, la aplicación puede ver una degradación del rendimiento.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Informe de errores de Windows entrada de blog](/archive/blogs/wer/)
-   [Servicios en línea de calidad de Windows (WinQual)](https://winqual.microsoft.com)

 

 
