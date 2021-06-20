---
title: Tipos con signo y sin signo (RPC)
description: Obtenga información sobre los tipos con y sin signo en RPC. Los compiladores que usan distintos tipos de valores predeterminados pueden producir errores de software en la aplicación distribuida.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406548"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="6674e-104">Tipos con signo y sin signo (RPC)</span><span class="sxs-lookup"><span data-stu-id="6674e-104">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="6674e-105">Los compiladores que usan valores predeterminados diferentes para tipos firmados y sin firmar pueden producir errores de software en la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="6674e-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="6674e-106">Puede evitar estos problemas declarando explícitamente los tipos de caracteres como **con** signo **o sin signo.**</span><span class="sxs-lookup"><span data-stu-id="6674e-106">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="6674e-107">MIDL define el [**tipo pequeño**](/windows/desktop/Midl/small) para tomar el mismo signo predeterminado que el **tipo char** en el compilador de C de destino.</span><span class="sxs-lookup"><span data-stu-id="6674e-107">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="6674e-108">Si el compilador asume que **char** no tiene signo, **small** también se definirá como unsigned.</span><span class="sxs-lookup"><span data-stu-id="6674e-108">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="6674e-109">Muchos compiladores de C permiten cambiar el valor predeterminado como una opción de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="6674e-109">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="6674e-110">Por ejemplo, la opción de línea de comandos **/J** del compilador de Microsoft C cambia el signo predeterminado de **char** de signed a unsigned.</span><span class="sxs-lookup"><span data-stu-id="6674e-110">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="6674e-111">También puede controlar el signo de variables de tipo **char** y **small** con el modificador de línea de comandos del compilador MIDL [**/char**](/windows/desktop/Midl/-char).</span><span class="sxs-lookup"><span data-stu-id="6674e-111">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="6674e-112">Este modificador permite especificar el signo predeterminado que usa el compilador.</span><span class="sxs-lookup"><span data-stu-id="6674e-112">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="6674e-113">El compilador MIDL declara explícitamente el signo de todos los tipos **char** que no coinciden con el tipo predeterminado del compilador de C en el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="6674e-113">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
