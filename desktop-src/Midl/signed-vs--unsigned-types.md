---
title: Tipos con signo y sin signo (MIDL)
description: Obtenga información sobre los tipos con y sin signo en MIDL. Los compiladores que usan diferentes tipos de valores predeterminados pueden producir errores de software en la aplicación distribuida.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipos de datos MIDL, con signo y sin signo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159386"
---
# <a name="signed-and-unsigned-types-midl"></a>Tipos con signo y sin signo (MIDL)

Los compiladores que usan valores predeterminados diferentes para tipos firmados y sin firmar pueden producir errores de software en la aplicación distribuida. Puede evitar estos problemas declarando explícitamente los tipos de caracteres como con signo o sin signo. Tenga en cuenta que los compiladores de IDL de DCE no reconocen la palabra clave [**signed**](signed.md). Por lo tanto, esta característica no está disponible cuando se usa el compilador MIDL /**modificador osf.**

MIDL define el [**tipo pequeño**](small.md) para tomar el mismo signo predeterminado que el [**tipo char**](char-idl.md) en el compilador de C de destino. Si el compilador da por supuesto **que char** no tiene signo, **small** también se definirá como unsigned. Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos. Por ejemplo, en el entorno Microsoft Visual C++ desarrollo, la opción de línea de **comandos /J** cambia el signo predeterminado de **char** de signed a unsigned.

También puede controlar el signo de variables de tipo [**char**](char-idl.md) y [**small**](small.md) con el modificador de línea de comandos del compilador MIDL [**/char**](-char.md). Este modificador permite especificar el signo predeterminado que usa el compilador. El compilador MIDL declara explícitamente el signo de todos los tipos **char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.

 

 




