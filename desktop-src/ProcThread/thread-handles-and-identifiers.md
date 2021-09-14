---
description: Cuando la función CreateThread o CreateRemoteThread crea un nuevo subproceso, se devuelve un identificador para el subproceso.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Identificadores e identificadores de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501d449bdb34d158ad14e52409967d4ef17f62f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062792"
---
# <a name="thread-handles-and-identifiers"></a>Identificadores e identificadores de subprocesos

Cuando la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) crea un nuevo subproceso, se devuelve un identificador para el subproceso. De forma predeterminada, este identificador tiene derechos de acceso completos y, sujeto a la comprobación de acceso de seguridad, se puede usar en cualquiera de las funciones que aceptan un identificador de subproceso. Los procesos secundarios pueden heredar este identificador, en función de la marca de herencia especificada cuando se crea. [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)puede duplicar el identificador, lo que le permite crear un identificador de subproceso con un subconjunto de los derechos de acceso. El identificador es válido hasta que se cierra, incluso después de que se haya terminado el subproceso que representa.

Las [**funciones CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) y [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) también devuelven un identificador que identifica de forma única el subproceso en todo el sistema. Un subproceso puede usar la [**función GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) para obtener su propio identificador de subproceso. Los identificadores son válidos desde el momento en que se crea el subproceso hasta que se ha terminado. Tenga en cuenta que ningún identificador de subproceso será nunca 0.

Si tiene un identificador de subproceso, puede obtener el identificador del subproceso llamando a la [**función OpenThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) **OpenThread** permite especificar los derechos de acceso del identificador y si se puede heredar.

Un subproceso puede usar la [**función GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) para recuperar un *pseudo identificador* en su propio objeto de subproceso. Este pseudo identificador solo es válido para el proceso de llamada; no se puede heredar ni duplicar para su uso por otros procesos. Para obtener el identificador real para el subproceso, dado un pseudo identificador, use la [**función DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

Para enumerar los subprocesos de un proceso, use las [**funciones Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) y [**Thread32Next.**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next)

 

 
