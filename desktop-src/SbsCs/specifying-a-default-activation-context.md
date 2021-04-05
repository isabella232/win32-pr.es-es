---
description: Especificar un contexto de activación predeterminado
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Especificar un contexto de activación predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cf0225a8e4290a09f7e6524a4b3ef47f9c4c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002764"
---
# <a name="specifying-a-default-activation-context"></a>Especificar un contexto de activación predeterminado

Cuando la aplicación o el componente crean un nuevo proceso, Windows busca un manifiesto de aplicación predeterminado. Tenga en cuenta que un manifiesto incluido como un recurso en la aplicación tiene prioridad sobre un manifiesto externo. El contexto de activación predeterminado es el primer contexto de activación que está activo antes de que se haya activado cualquier otro contexto de activación. Este contexto de activación siempre está activo a menos que Active otros contextos. Si define \_ \_ el reconocimiento de aislamiento habilitado al compilar la aplicación o el componente, llamadas como [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)y [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pueden realizar la administración automática del contexto.

El cargador permite que una aplicación especifique su contexto de activación predeterminado mediante dos métodos. Puede colocar el archivo de manifiesto en los recursos del archivo ejecutable y el cargador lo encontrará. Esto es lo mismo que colocar el archivo de manifiesto en la tabla de recursos del archivo ejecutable. Puede colocar el manifiesto en un archivo denominado *MyApp*. exe. Manifest en el mismo directorio que *MyApp*. exe y el cargador lo encuentra al buscar *MyApp*. exe.

Si utiliza ninguno de estos métodos, la aplicación se inicia con el contexto de activación predeterminado del sistema, que contiene un conjunto mínimo de ensamblados.

Una manera mejor de usar la administración automática de contexto es compilando la aplicación con el reconocimiento de aislamiento \_ \_ habilitado definido. El método recomendado es establecer esto en la línea de comandos del compilador para todo el proyecto que se compila en lugar de establecerse en archivos de código fuente o encabezados individuales. Esto hace que la mayoría de las API de Win32 conozcan los contextos de activación y cómo administrarlos. En lugar de tener que realizar su propia administración de contexto de activación, solo tiene que colocar un manifiesto en la tabla de recursos en el ID. \_ de recurso del manifiesto ISOLATIONAWARE \_ \_ (valor numérico 2), de tipo RT \_ manifest (valor numérico 24). Las funciones como [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)y [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) activan este contexto automáticamente antes de efectuar la llamada real.

Tenga en cuenta que si se compila con \_ el reconocimiento de aislamiento \_ habilitado, no se puede realizar su propia administración de contexto de activación. Con el \_ reconocimiento de aislamiento \_ habilitado, Windows omite cualquier creación de contexto de activación dinámica que la aplicación pueda intentar realizar entre las llamadas a [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) y [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . Esto significa que cuando la aplicación usa el \_ reconocimiento de aislamiento \_ habilitado, debe asegurarse de que el manifiesto contiene una lista completa de todos los ensamblados que requiere el componente.

 

 
