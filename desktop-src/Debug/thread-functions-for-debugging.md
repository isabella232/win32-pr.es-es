---
description: Aprenda a usar la función CreateThread para crear un subproceso para un proceso. Normalmente, los depuradores deben examinar o cambiar el contenido de los registros de un subproceso.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funciones de subproceso para la depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403988"
---
# <a name="thread-functions-for-debugging"></a>Funciones de subproceso para la depuración

La [**función CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuevo subproceso para un proceso. Normalmente, los depuradores deben examinar o cambiar el contenido de los registros de un subproceso. Para ello, un depurador debe obtener un identificador para el subproceso mediante la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) y especificar el acceso adecuado al subproceso (THREAD GET CONTEXT, THREAD SET CONTEXT o \_ \_ \_ \_ ambos). La [**función OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite a un depurador obtener el identificador de un subproceso existente.

Un proceso con acceso adecuado a un subproceso puede examinar los registros del subproceso mediante la función [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) y establecer el contenido de los registros del subproceso mediante la [**función SetThreadContext.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)

Un proceso también puede obtener acceso \_ THREAD SUSPEND RESUME a un \_ subproceso. Este tipo de acceso permite a un depurador controlar la ejecución de un subproceso con las [**funciones SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) [**y ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) Para obtener más información sobre los subprocesos, [vea Procesos y subprocesos.](../procthread/processes-and-threads.md)

 

 
