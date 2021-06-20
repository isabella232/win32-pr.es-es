---
title: Tipos con signo y sin signo (MIDL)
description: Obtenga información sobre los tipos firmados y sin firmar en MIDL. Los compiladores que usan diferentes tipos de valores predeterminados pueden producir errores de software en la aplicación distribuida.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipos de datos MIDL, signed y unsigned
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407388"
---
# <a name="signed-and-unsigned-types-midl"></a>Tipos con signo y sin signo (MIDL)

Los compiladores que usan valores predeterminados diferentes para los tipos firmados y sin firmar pueden producir errores de software en la aplicación distribuida. Puede evitar estos problemas declarando explícitamente los tipos de caracteres como con signo o sin signo. Tenga en cuenta que los compiladores de IDL de DCE no reconocen la palabra clave [**signed**](signed.md). Por lo tanto, esta característica no está disponible cuando se usa el compilador MIDL o **el modificador osf.**

MIDL define el [**tipo pequeño**](small.md) para que tome el mismo signo predeterminado que el [**tipo char**](char-idl.md) en el compilador de C de destino. Si el compilador asume que **char** no tiene signo, **small** también se definirá como unsigned. Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos. Por ejemplo, en el entorno Microsoft Visual C++ desarrollo, la opción de línea de comandos **/J** cambia el signo predeterminado de **char** de signed a unsigned.

También puede controlar el signo de variables de tipo [**char**](char-idl.md) y [**small**](small.md) con el modificador de línea de comandos del compilador MIDL [**/char**](-char.md). Este modificador permite especificar el signo predeterminado que usa el compilador. El compilador MIDL declara explícitamente el signo de todos los tipos **char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.

 

 




