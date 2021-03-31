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
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="d348f-103">Tipos con signo y sin signo (RPC)</span><span class="sxs-lookup"><span data-stu-id="d348f-103">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="d348f-104">Los compiladores que usan valores predeterminados diferentes para los tipos con signo y sin signo pueden producir errores de software en la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="d348f-104">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="d348f-105">Puede evitar estos problemas declarando explícitamente los tipos de caracteres como **con signo** o **sin signo**.</span><span class="sxs-lookup"><span data-stu-id="d348f-105">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="d348f-106">MIDL define el tipo [**pequeño**](/windows/desktop/Midl/small) para que tenga el mismo signo predeterminado que el tipo **Char** en el compilador de C de destino.</span><span class="sxs-lookup"><span data-stu-id="d348f-106">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="d348f-107">Si el compilador supone que **Char** es sin signo, **Small** también se definirá como sin signo.</span><span class="sxs-lookup"><span data-stu-id="d348f-107">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="d348f-108">Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d348f-108">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="d348f-109">Por ejemplo, la opción de línea de comandos del compilador de Microsoft C **/j** cambia el signo predeterminado de **Char** de signed a Unsigned.</span><span class="sxs-lookup"><span data-stu-id="d348f-109">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="d348f-110">También puede controlar el signo de las variables de tipo **Char** y **Small** con el modificador de línea de comandos del compilador MIDL [**/Char**](/windows/desktop/Midl/-char).</span><span class="sxs-lookup"><span data-stu-id="d348f-110">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="d348f-111">Este modificador le permite especificar el signo predeterminado que usa el compilador.</span><span class="sxs-lookup"><span data-stu-id="d348f-111">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="d348f-112">El compilador MIDL declara explícitamente el signo de todos los tipos **Char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="d348f-112">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
