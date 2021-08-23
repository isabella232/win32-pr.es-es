---
description: Cuando se produce una excepción en un proceso que se está depurando, el sistema notifica al depurador pasando la excepción a él. Esto se conoce como notificación de primera oportunidad. A continuación, el sistema suspende todos los subprocesos del proceso que se está depurando.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funciones de control de excepciones para la depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4542b6e1d3ad2699b3cb43d15e327d26156760980188555b1a4bf9c68e9a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573175"
---
# <a name="exception-handling-functions-for-debugging"></a>Funciones de control de excepciones para la depuración

Cuando se produce una excepción en un proceso que se está depurando, el sistema notifica al depurador pasando la excepción a él. Esto se conoce como notificación *de primera oportunidad.* A continuación, el sistema suspende todos los subprocesos del proceso que se está depurando.

Si el depurador no controla la excepción, el sistema intenta buscar un controlador de excepciones adecuado. Si el sistema no encuentra uno adecuado, el sistema notifica de nuevo al depurador que se ha producido una excepción. Esto se conoce como *notificación de última oportunidad.* Si el depurador no controla la excepción después de la notificación de última oportunidad, el sistema finaliza el proceso que se está depurando.

Para obtener más información, vea [Control de excepciones del depurador.](debugger-exception-handling.md)

 

 



