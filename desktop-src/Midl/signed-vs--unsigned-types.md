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
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="48d5c-105">Tipos con signo y sin signo (MIDL)</span><span class="sxs-lookup"><span data-stu-id="48d5c-105">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="48d5c-106">Los compiladores que usan valores predeterminados diferentes para los tipos firmados y sin firmar pueden producir errores de software en la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="48d5c-106">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="48d5c-107">Puede evitar estos problemas declarando explícitamente los tipos de caracteres como con signo o sin signo.</span><span class="sxs-lookup"><span data-stu-id="48d5c-107">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="48d5c-108">Tenga en cuenta que los compiladores de IDL de DCE no reconocen la palabra clave [**signed**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="48d5c-108">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="48d5c-109">Por lo tanto, esta característica no está disponible cuando se usa el compilador MIDL o **el modificador osf.**</span><span class="sxs-lookup"><span data-stu-id="48d5c-109">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="48d5c-110">MIDL define el [**tipo pequeño**](small.md) para que tome el mismo signo predeterminado que el [**tipo char**](char-idl.md) en el compilador de C de destino.</span><span class="sxs-lookup"><span data-stu-id="48d5c-110">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="48d5c-111">Si el compilador asume que **char** no tiene signo, **small** también se definirá como unsigned.</span><span class="sxs-lookup"><span data-stu-id="48d5c-111">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="48d5c-112">Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="48d5c-112">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="48d5c-113">Por ejemplo, en el entorno Microsoft Visual C++ desarrollo, la opción de línea de comandos **/J** cambia el signo predeterminado de **char** de signed a unsigned.</span><span class="sxs-lookup"><span data-stu-id="48d5c-113">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="48d5c-114">También puede controlar el signo de variables de tipo [**char**](char-idl.md) y [**small**](small.md) con el modificador de línea de comandos del compilador MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="48d5c-114">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="48d5c-115">Este modificador permite especificar el signo predeterminado que usa el compilador.</span><span class="sxs-lookup"><span data-stu-id="48d5c-115">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="48d5c-116">El compilador MIDL declara explícitamente el signo de todos los tipos **char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="48d5c-116">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




