---
description: Aprenda a usar la función CreateThread para crear un subproceso para un proceso. Normalmente, los depuradores deben examinar o cambiar el contenido de los registros de un subproceso.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funciones de subproceso para la depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e9c94ef776cd14bc76afb2c824f2150a1e7c0eb8c94176b237e1c6d54430f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655225"
---
# <a name="thread-functions-for-debugging"></a>Funciones de subproceso para la depuración

La [**función CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuevo subproceso para un proceso. Normalmente, los depuradores deben examinar o cambiar el contenido de los registros de un subproceso. Para ello, un depurador debe obtener un identificador para el subproceso mediante la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) y especificar el acceso adecuado al subproceso (THREAD GET CONTEXT, THREAD SET CONTEXT o \_ \_ \_ \_ ambos). La [**función OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite que un depurador obtenga el identificador de un subproceso existente.

Un proceso con acceso adecuado a un subproceso puede examinar los registros del subproceso mediante la función [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) y establecer el contenido de los registros del subproceso mediante la [**función SetThreadContext.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)

Un proceso también puede obtener el acceso \_ SUSPEND RESUME de SUBPROCESO a un \_ subproceso. Este tipo de acceso permite a un depurador controlar la ejecución de un subproceso con las [**funciones SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) [**y ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) Para obtener más información sobre los subprocesos, vea [Procesos y subprocesos](../procthread/processes-and-threads.md).

 

 
