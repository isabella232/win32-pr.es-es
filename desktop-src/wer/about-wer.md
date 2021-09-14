---
title: Acerca de WER
description: Informe de errores de Windows (WER) es una infraestructura flexible de comentarios basada en eventos diseñada para recopilar información sobre los problemas de hardware y software que Windows puede detectar, notificar la información a Microsoft y proporcionar a los usuarios las soluciones disponibles. Para obtener información sobre las mejoras de WER, consulte Novedades de WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Windows informe de errores Informe de errores de Windows , acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256514"
---
# <a name="about-wer"></a>Acerca de WER

Informe de errores de Windows (WER) es una infraestructura flexible de comentarios basada en eventos diseñada para recopilar información sobre los problemas de hardware y software que Windows puede detectar, notificar la información a Microsoft y proporcionar a los usuarios las soluciones disponibles. Para obtener información sobre las mejoras de WER, vea [Novedades de WER.](what-s-new-in-wer.md)

A partir de Windows Vista, Windows proporciona informes de errores de bloqueo, sin respuesta y de error de kernel de forma predeterminada sin necesidad de realizar cambios en la aplicación. En su lugar, las aplicaciones usan la API de WER para generar informes de errores para problemas específicos de la aplicación que no están relacionados con bloqueos, no respuestas o errores de kernel.

Para generar informes de errores para problemas específicos de la aplicación, la aplicación debe crear una breve descripción del problema mediante algunos fragmentos básicos de información denominados *parámetros de informe*. Los parámetros de informe incluyen información como el nombre de la aplicación, la versión de la aplicación, el nombre del módulo, la versión del módulo y el código de error. La combinación de estos parámetros de informe describe un problema único.

Cuando WER busca una solución, se comunica con el servidor WER en Microsoft; para ello, primero pregunta si el problema ya se conoce. El servidor responde de una de las maneras siguientes:

-   Si se conoce el problema y hay una solución, el servidor envía la solución al equipo cliente y WER muestra esta información al usuario.
-   Si se está investigando el problema, el servidor puede enviar una respuesta que indique el estado. Si el desarrollador necesita más información para resolver el problema, el servidor solicita información adicional de WER y WER solicita al usuario permiso para enviar esta información.
-   Si no se conoce el problema, el servidor crea un problema para que un desarrollador investigue y envía a WER una respuesta que indica el estado.

Con este proceso, WER recopila más información si es necesario o envía una solución al usuario cuando está disponible. En Windows Vista, el usuario puede  ir a Informes de problemas y soluciones en cualquier momento para ver las soluciones disponibles, comprobar si hay nuevas soluciones disponibles o administrar sus otros informes y configuraciones de WER. En Windows 7, los **informes de** problemas y las soluciones ahora se denominan centro de **acciones.** Haga **clic en** Inicio  y escriba "ver" en Buscar programas y archivos **y, a continuación,** seleccione Ver todo informes de **problemas,** Ver historial de confiabilidad o Ver soluciones a **problemas.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Informe de errores de Windows](windows-error-reporting.md)
</dt> </dl>

 

 




