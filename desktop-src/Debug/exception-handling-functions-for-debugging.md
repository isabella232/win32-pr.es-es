---
description: Cuando se produce una excepción en un proceso que se está depurando, el sistema notifica al depurador pasando la excepción a él. Esto se conoce como notificación de primera oportunidad. Después, el sistema suspende todos los subprocesos del proceso que se está depurando.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Funciones de control de excepciones para la depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906924"
---
# <a name="exception-handling-functions-for-debugging"></a>Funciones de control de excepciones para la depuración

Cuando se produce una excepción en un proceso que se está depurando, el sistema notifica al depurador pasando la excepción a él. Esto se conoce como *notificación de primera oportunidad*. Después, el sistema suspende todos los subprocesos del proceso que se está depurando.

Si el depurador no controla la excepción, el sistema intenta encontrar un controlador de excepciones adecuado. Si el sistema no encuentra uno adecuado, el sistema notifica de nuevo al depurador que se ha producido una excepción. Esto se conoce como *notificación de última oportunidad*. Si el depurador no controla la excepción después de la notificación de última oportunidad, el sistema finaliza el proceso que se está depurando.

Para obtener más información, vea [control de excepciones del depurador](debugger-exception-handling.md).

 

 



