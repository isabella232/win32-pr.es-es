---
description: Cuando se crea un nuevo subproceso mediante la función CreateThread o CreateRemoteThread, se devuelve un identificador al subproceso.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Identificadores e identificadores de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501d449bdb34d158ad14e52409967d4ef17f62f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909673"
---
# <a name="thread-handles-and-identifiers"></a>Identificadores e identificadores de subprocesos

Cuando se crea un nuevo subproceso mediante la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) , se devuelve un identificador al subproceso. De forma predeterminada, este identificador tiene derechos de acceso completo y, en función de la comprobación de acceso de seguridad, se puede usar en cualquiera de las funciones que aceptan un identificador de subproceso. Este identificador lo pueden heredar los procesos secundarios, dependiendo del indicador de herencia especificado al crearlo. El identificador se puede duplicar mediante [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle), lo que permite crear un identificador de subproceso con un subconjunto de derechos de acceso. El identificador es válido hasta que se cierra, incluso después de que se haya terminado el subproceso que representa.

Las funciones [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) y [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) también devuelven un identificador que identifica de forma única el subproceso en todo el sistema. Un subproceso puede utilizar la función [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) para obtener su propio identificador de subproceso. Los identificadores son válidos desde el momento en que se crea el subproceso hasta que el subproceso haya finalizado. Tenga en cuenta que ningún identificador de subproceso nunca será 0.

Si tiene un identificador de subproceso, puede obtener el identificador de subproceso mediante una llamada a la función [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) . **OpenThread** permite especificar los derechos de acceso del identificador y si puede heredarse.

Un subproceso puede usar la función [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) para recuperar un *pseudo identificador* de su propio objeto de subproceso. Este pseudo identificador solo es válido para el proceso de llamada; no se puede heredar ni duplicar para su uso por parte de otros procesos. Para obtener el identificador real del subproceso, dado un pseudo identificador, utilice la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Para enumerar los subprocesos de un proceso, utilice las funciones [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) y [**Thread32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next) .

 

 
