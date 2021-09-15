---
title: Tipos con signo y sin signo (RPC)
description: Obtenga información sobre los tipos firmados y sin firmar en RPC. Los compiladores que usan diferentes tipos de valores predeterminados pueden producir errores de software en la aplicación distribuida.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473519"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipos con signo y sin signo (RPC)

Los compiladores que usan valores predeterminados diferentes para los tipos firmados y sin firmar pueden producir errores de software en la aplicación distribuida. Puede evitar estos problemas declarando explícitamente los tipos de caracteres como **con signo** o **sin signo.**

MIDL define el [**tipo pequeño**](/windows/desktop/Midl/small) para que tome el mismo signo predeterminado que el **tipo char** en el compilador de C de destino. Si el compilador asume que **char** no tiene signo, **small** también se definirá como unsigned. Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos. Por ejemplo, la opción de línea de comandos **/J** del compilador de Microsoft C cambia el signo predeterminado de **char** de signed a unsigned.

También puede controlar el signo de variables de tipo **char** y **small** con el modificador de línea de comandos del compilador MIDL [**/char**](/windows/desktop/Midl/-char). Este modificador permite especificar el signo predeterminado que usa el compilador. El compilador MIDL declara explícitamente el signo de todos los tipos **char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.

 

 
