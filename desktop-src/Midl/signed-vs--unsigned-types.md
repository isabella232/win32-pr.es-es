---
title: Tipos con signo y sin signo (MIDL)
description: Los compiladores que usan valores predeterminados diferentes para los tipos con signo y sin signo pueden producir errores de software en la aplicación distribuida.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipos de datos MIDL, con signo y sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421759"
---
# <a name="signed-and-unsigned-types-midl"></a>Tipos con signo y sin signo (MIDL)

Los compiladores que usan valores predeterminados diferentes para los tipos con signo y sin signo pueden producir errores de software en la aplicación distribuida. Puede evitar estos problemas declarando explícitamente los tipos de caracteres como con signo o sin signo. Tenga en cuenta que los compiladores de DCE IDL no reconocen la palabra clave [**signed**](signed.md). Por lo tanto, esta característica no está disponible cuando se usa el modificador/**OSF** del compilador MIDL.

MIDL define el tipo [**pequeño**](small.md) para que tenga el mismo signo predeterminado que el tipo [**Char**](char-idl.md) en el compilador de C de destino. Si el compilador supone que **Char** es sin signo, **Small** también se definirá como sin signo. Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos. Por ejemplo, en el entorno de desarrollo de Microsoft Visual C++, la opción de línea de comandos **/j** cambia el signo predeterminado de **Char** de signed a Unsigned.

También puede controlar el signo de las variables de tipo [**Char**](char-idl.md) y [**Small**](small.md) con el modificador de línea de comandos del compilador MIDL [**/Char**](-char.md). Este modificador le permite especificar el signo predeterminado que usa el compilador. El compilador MIDL declara explícitamente el signo de todos los tipos **Char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.

 

 




