---
description: Informe de errores de Windows Grabación de acciones de usuario
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Informe de errores de Windows Grabación de acciones de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084163"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Informe de errores de Windows Grabación de acciones de usuario

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  


## <a name="description"></a>Descripción

Antes de Windows 7, Informe de errores de Windows (WER) recopilaba informes de errores que indicaban problemas que necesitaban reparación. Estos informes de error contienen información útil que describe la naturaleza general de un problema, pero no suficiente información para determinar su causa principal. Para ello, los desarrolladores necesitan una herramienta para reproducir el escenario de bloqueo o bloqueo para la depuración.

Una nueva aplicación, Grabación de acciones de usuario (PSR.exe), se está enviando en todas las compilaciones de Windows 7. Esta característica permite la recopilación de las acciones realizadas por un usuario al encontrar un bloqueo para que los evaluadores y desarrolladores puedan reproducir la situación para su análisis y depuración.

## <a name="usage"></a>Uso

Actualmente, un desarrollador Informe de errores de Windows servicio debe solicitar la habilitación de PSR para una aplicación; Las organizaciones de soporte técnico de Microsoft también usan esta herramienta al solucionar problemas con los usuarios finales. Hay planes para que PSR esté disponible en Windows Quality Online Services (Winqual) después del lanzamiento de Windows 7.

**Nota:** Con PSR habilitado para una aplicación, es posible que la aplicación vea alguna degradación del rendimiento.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Informe de errores de Windows entrada de blog](/archive/blogs/wer/)
-   [Windows Quality Online Services (Winqual)](https://winqual.microsoft.com)

 

 
