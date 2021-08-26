---
title: Suplantación y llamadas asincrónicas
description: Suplantación y llamadas asincrónicas
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84f7fcbdc820b50ef4eaaedd81ac579fcce64f1371bc57219348f6dcbedc0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070885"
---
# <a name="impersonation-and-asynchronous-calls"></a>Suplantación y llamadas asincrónicas

El servidor no puede suplantar al cliente después de que se complete la llamada del servidor a [**ISynchronize::Signal,**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) incluso si el método Begin aún no \_ se ha completado. Por ejemplo, suponga que un cliente llama al método Begin, el servidor procesa la llamada inmediatamente y el servidor llama a Signal para indicar que ha finalizado \_ el procesamiento.  Incluso si queda trabajo por realizar en el método Begin, el servidor no puede suplantar al cliente una vez completada la llamada \_ a **Signal.**

Si el servidor suplanta al cliente antes de llamar a [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), el token de suplantación no se quitará del subproceso hasta que el servidor llame a [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) o hasta que se devuelva la llamada del servidor a Begin, lo que pase \_ primero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delegación y suplantación](delegation-and-impersonation.md)
</dt> <dt>

[Realizar una llamada asincrónica](making-an-asynchronous-call.md)
</dt> </dl>

 

 