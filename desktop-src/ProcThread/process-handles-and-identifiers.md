---
description: Cuando la función CreateProcess crea un nuevo proceso, se devuelven los identificadores del nuevo proceso y su subproceso principal.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Identificadores e identificadores de proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a1ec0acb6535f8f64b9f4bd0815392d61fccbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360688"
---
# <a name="process-handles-and-identifiers"></a>Identificadores e identificadores de proceso

Cuando la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) crea un nuevo proceso, se devuelven los identificadores del nuevo proceso y su subproceso principal. Estos identificadores se crean con derechos de acceso completo y, en función de la comprobación de acceso de seguridad, se pueden usar en cualquiera de las funciones que aceptan identificadores de subprocesos o procesos. Estos identificadores pueden ser heredados por procesos secundarios, en función del indicador de herencia especificado cuando se crean. Los identificadores son válidos hasta que se cierran, incluso después de finalizar el proceso o subproceso que representan.

La función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) también devuelve un identificador que identifica de forma única el proceso en todo el sistema. Un proceso puede usar la función [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) para obtener su propio identificador de proceso (también conocido como identificador de proceso o PID). El identificador es válido desde el momento en que se crea el proceso hasta que se termina el proceso. Un proceso puede utilizar la función [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) para obtener el identificador de proceso de su proceso primario.

Si tiene un identificador de proceso, puede obtener el identificador de proceso mediante una llamada a la función [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) . **OpenProcess** le permite especificar los derechos de acceso del identificador y si puede heredarse.

Un proceso puede usar la función [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) para recuperar un pseudo identificador de su propio objeto de proceso. Este pseudo identificador solo es válido para el proceso de llamada; no se puede heredar ni duplicar para su uso por parte de otros procesos. Para obtener el identificador real del proceso, llame a la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

 

 
