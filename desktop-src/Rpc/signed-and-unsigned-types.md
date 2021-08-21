---
title: Tipos con signo y sin signo (RPC)
description: Obtenga información sobre los tipos con y sin signo en RPC. Los compiladores que usan diferentes tipos de valores predeterminados pueden producir errores de software en la aplicación distribuida.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17a2ccf28233bb14e0811e8015c83aede37d60c58fe9411f13806355fdb7f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017705"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipos con signo y sin signo (RPC)

Los compiladores que usan valores predeterminados diferentes para tipos firmados y sin signo pueden provocar errores de software en la aplicación distribuida. Puede evitar estos problemas declarando explícitamente los tipos de caracteres como **con** signo **o sin signo.**

MIDL define el [**tipo pequeño**](/windows/desktop/Midl/small) para tomar el mismo signo predeterminado que el **tipo char** en el compilador de C de destino. Si el compilador asume que **char** no tiene signo, **small** también se definirá como unsigned. Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos. Por ejemplo, la opción de línea de comandos **/J** del compilador de Microsoft C cambia el signo predeterminado de **char** de signed a unsigned.

También puede controlar el signo de variables de tipo **char** y **small** con el modificador de línea de comandos del compilador MIDL [**/char**](/windows/desktop/Midl/-char). Este modificador permite especificar el signo predeterminado que usa el compilador. El compilador MIDL declara explícitamente el signo de todos los tipos **char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.

 

 
