---
title: Suplantación y llamadas asincrónicas
description: Suplantación y llamadas asincrónicas
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794158"
---
# <a name="impersonation-and-asynchronous-calls"></a>Suplantación y llamadas asincrónicas

El servidor no puede suplantar al cliente después de que se complete la llamada del servidor a [**ISynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) , aunque \_ no se haya completado aún el método Begin. Por ejemplo, supongamos que un cliente llama al \_ método Begin, el servidor procesa la llamada inmediatamente y el servidor llama a **Signal** para indicar que ha finalizado el procesamiento. Aunque el trabajo siga siendo realizado en el método Begin \_ , el servidor no puede suplantar al cliente después de que se complete la llamada a **Signal** .

Si el servidor suplanta al cliente antes de llamar a [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), el token de suplantación no se quitará del subproceso hasta que el servidor llame a [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) o hasta que la llamada del servidor a Begin vuelva, lo que suceda \_ primero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delegación y suplantación](delegation-and-impersonation.md)
</dt> <dt>

[Realización de una llamada asincrónica](making-an-asynchronous-call.md)
</dt> </dl>

 

 