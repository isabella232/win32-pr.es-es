---
title: Tipos con signo y sin signo (RPC)
description: Los compiladores que usan valores predeterminados diferentes para los tipos con signo y sin signo pueden producir errores de software en la aplicación distribuida.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904956"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipos con signo y sin signo (RPC)

Los compiladores que usan valores predeterminados diferentes para los tipos con signo y sin signo pueden producir errores de software en la aplicación distribuida. Puede evitar estos problemas declarando explícitamente los tipos de caracteres como **con signo** o **sin signo**.

MIDL define el tipo [**pequeño**](/windows/desktop/Midl/small) para que tenga el mismo signo predeterminado que el tipo **Char** en el compilador de C de destino. Si el compilador supone que **Char** es sin signo, **Small** también se definirá como sin signo. Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos. Por ejemplo, la opción de línea de comandos del compilador de Microsoft C **/j** cambia el signo predeterminado de **Char** de signed a Unsigned.

También puede controlar el signo de las variables de tipo **Char** y **Small** con el modificador de línea de comandos del compilador MIDL [**/Char**](/windows/desktop/Midl/-char). Este modificador le permite especificar el signo predeterminado que usa el compilador. El compilador MIDL declara explícitamente el signo de todos los tipos **Char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.

 

 
