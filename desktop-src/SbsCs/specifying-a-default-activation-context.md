---
description: Especificar un contexto de activación predeterminado
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Especificar un contexto de activación predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cf0225a8e4290a09f7e6524a4b3ef47f9c4c4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073800"
---
# <a name="specifying-a-default-activation-context"></a>Especificar un contexto de activación predeterminado

Cuando la aplicación o el componente crea un nuevo proceso, Windows busca un manifiesto de aplicación predeterminado. Tenga en cuenta que un manifiesto incluido como recurso en la aplicación tiene prioridad sobre un manifiesto externo. El contexto de activación predeterminado es el primer contexto de activación que está activo antes de que se haya activado cualquier otro contexto de activación. Este contexto de activación siempre está activo a menos que active otros contextos. Si define ISOLATION AWARE ENABLED al compilar la aplicación o componente, llamadas como \_ \_ [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)y [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pueden realizar la administración automática de contexto.

El cargador permite que una aplicación especifique su contexto de activación predeterminado mediante dos métodos. Puede colocar el archivo de manifiesto en los recursos del ejecutable y el cargador lo encontrará. Esto es lo mismo que colocar el archivo de manifiesto en la tabla de recursos del ejecutable. Puede colocar el manifiesto en un archivo denominado *Myapp*.exe. Manifiesto en el mismo directorio que *Myapp*.exe y el cargador lo encuentra al buscar *Myapp*.exe.

Si no usa ninguno de estos métodos, la aplicación se inicia con el contexto de activación predeterminado del sistema, que contiene un conjunto mínimo de ensamblados.

Una mejor manera de usar la administración automática de contexto es compilar la aplicación con ISOLATION \_ AWARE \_ ENABLED definido. El método recomendado consiste en establecer esto en la línea de comandos del compilador para todo el proyecto que se está compilando en lugar de establecerse en encabezados o archivos de código fuente individuales. Esto hace que la mayoría de las API de Win32 conozcan los contextos de activación y cómo administrarlos. En lugar de tener que realizar su propia administración del contexto de activación, basta con colocar un manifiesto en la tabla de recursos en id. de recurso ISOLATIONAWARE MANIFEST RESOURCE ID (valor numérico 2), de tipo \_ RT MANIFEST \_ \_ \_ (valor numérico 24). Funciones como [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)y [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) activan automáticamente este contexto antes de realizar la llamada real.

Tenga en cuenta que si compila con ISOLATION AWARE ENABLED definido, tampoco puede realizar \_ su propia administración del contexto de \_ activación. Con ISOLATION AWARE ENABLED definido, Windows omitir cualquier creación de contexto de activación dinámica que la aplicación pueda intentar realizar entre las llamadas \_ \_ [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) y [**CreateWindow.**](/windows/win32/api/winuser/nf-winuser-createwindowa) Esto significa que cuando la aplicación usa ISOLATION AWARE ENABLED, debe asegurarse de que el manifiesto contiene una lista completa de todos los ensamblados que \_ \_ requiere el componente.

 

 
