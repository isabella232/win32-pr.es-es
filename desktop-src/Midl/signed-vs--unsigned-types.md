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
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="cf0f2-104">Tipos con signo y sin signo (MIDL)</span><span class="sxs-lookup"><span data-stu-id="cf0f2-104">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="cf0f2-105">Los compiladores que usan valores predeterminados diferentes para los tipos con signo y sin signo pueden producir errores de software en la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="cf0f2-106">Puede evitar estos problemas declarando explícitamente los tipos de caracteres como con signo o sin signo.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-106">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="cf0f2-107">Tenga en cuenta que los compiladores de DCE IDL no reconocen la palabra clave [**signed**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="cf0f2-107">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="cf0f2-108">Por lo tanto, esta característica no está disponible cuando se usa el modificador/**OSF** del compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-108">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="cf0f2-109">MIDL define el tipo [**pequeño**](small.md) para que tenga el mismo signo predeterminado que el tipo [**Char**](char-idl.md) en el compilador de C de destino.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-109">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="cf0f2-110">Si el compilador supone que **Char** es sin signo, **Small** también se definirá como sin signo.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-110">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="cf0f2-111">Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-111">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="cf0f2-112">Por ejemplo, en el entorno de desarrollo de Microsoft Visual C++, la opción de línea de comandos **/j** cambia el signo predeterminado de **Char** de signed a Unsigned.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-112">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="cf0f2-113">También puede controlar el signo de las variables de tipo [**Char**](char-idl.md) y [**Small**](small.md) con el modificador de línea de comandos del compilador MIDL [**/Char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="cf0f2-113">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="cf0f2-114">Este modificador le permite especificar el signo predeterminado que usa el compilador.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-114">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="cf0f2-115">El compilador MIDL declara explícitamente el signo de todos los tipos **Char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="cf0f2-115">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




