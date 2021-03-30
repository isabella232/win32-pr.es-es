---
description: La función CreateThread crea un nuevo subproceso para un proceso.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funciones de subproceso para depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538907"
---
# <a name="thread-functions-for-debugging"></a>Funciones de subproceso para depuración

La función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuevo subproceso para un proceso. Los depuradores normalmente necesitan examinar o cambiar el contenido de los registros de un subproceso. Para ello, un depurador debe obtener un identificador para el subproceso mediante la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) y especificar el acceso adecuado al subproceso (contexto get del subproceso, \_ \_ \_ contexto del conjunto de subprocesos \_ o ambos). La función [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permite a un depurador obtener el identificador de un subproceso existente.

Un proceso con acceso adecuado a un subproceso puede examinar los registros del subproceso mediante la función [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) y establecer el contenido de los registros del subproceso mediante la función [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .

Un proceso también puede obtener el \_ acceso a la suspensión de SUBprocesos \_ para reanudar el acceso a un subproceso. Este tipo de acceso permite a un depurador controlar la ejecución de un subproceso con las funciones [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) y [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) . Para obtener más información sobre los subprocesos, vea [procesos y subprocesos](../procthread/processes-and-threads.md).

 

 
