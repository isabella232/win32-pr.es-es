---
title: Directivas de preprocesador (HLSL)
description: Las directivas de preprocesador, como \ define y \ ifdef, se usan normalmente para que los programas de origen sean fáciles de cambiar y fáciles de compilar en diferentes entornos de ejecución.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386834"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="f51e4-103">Directivas de preprocesador (HLSL)</span><span class="sxs-lookup"><span data-stu-id="f51e4-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="f51e4-104">Las directivas de preprocesador, como [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef,](dx-graphics-hlsl-appendix-pre-ifdef.md)se usan normalmente para que los programas de origen sean fáciles de cambiar y fáciles de compilar en diferentes entornos de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f51e4-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="f51e4-105">Las directivas del archivo de código fuente indican al preprocesador que realice acciones específicas.</span><span class="sxs-lookup"><span data-stu-id="f51e4-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="f51e4-106">Por ejemplo, el preprocesador puede reemplazar tokens en el texto, insertar el contenido de otros archivos en el archivo de código fuente o suprimir la compilación de parte del archivo quitando secciones de texto.</span><span class="sxs-lookup"><span data-stu-id="f51e4-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="f51e4-107">Las líneas de preprocesador se reconocen y se ejecutan antes de la expansión de macro.</span><span class="sxs-lookup"><span data-stu-id="f51e4-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="f51e4-108">Por consiguiente, si una macro se expande en algo que se parezca a un comando de preprocesador, el preprocesador no reconocerá ese comando.</span><span class="sxs-lookup"><span data-stu-id="f51e4-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="f51e4-109">Las instrucciones de preprocesador utilizan el mismo juego de caracteres que las instrucciones del archivo de código fuente, con la excepción de que no se admiten secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="f51e4-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="f51e4-110">El juego de caracteres utilizado en las instrucciones de preprocesador es el mismo que el juego de caracteres de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="f51e4-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="f51e4-111">El preprocesador también reconoce valores de caracteres negativos.</span><span class="sxs-lookup"><span data-stu-id="f51e4-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="f51e4-112">El preprocesador HLSL reconoce las siguientes directivas:</span><span class="sxs-lookup"><span data-stu-id="f51e4-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="f51e4-113">\#Definir</span><span class="sxs-lookup"><span data-stu-id="f51e4-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="f51e4-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="f51e4-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f51e4-115">\#else</span><span class="sxs-lookup"><span data-stu-id="f51e4-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f51e4-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="f51e4-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f51e4-117">\#Error</span><span class="sxs-lookup"><span data-stu-id="f51e4-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="f51e4-118">\#Si</span><span class="sxs-lookup"><span data-stu-id="f51e4-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f51e4-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="f51e4-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="f51e4-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="f51e4-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="f51e4-121">\#incluír</span><span class="sxs-lookup"><span data-stu-id="f51e4-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="f51e4-122">\#line</span><span class="sxs-lookup"><span data-stu-id="f51e4-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="f51e4-123">\#Pragma</span><span class="sxs-lookup"><span data-stu-id="f51e4-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="f51e4-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="f51e4-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="f51e4-125">El signo de número ( ) debe ser el primer carácter de espacio no blanco en la línea que contiene la directiva; los caracteres de espacio en blanco pueden aparecer entre el signo de número y la primera letra de \# la directiva.</span><span class="sxs-lookup"><span data-stu-id="f51e4-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="f51e4-126">Algunas directivas incluyen argumentos o valores.</span><span class="sxs-lookup"><span data-stu-id="f51e4-126">Some directives include arguments or values.</span></span> <span data-ttu-id="f51e4-127">Cualquier texto que sigue a una directiva (excepto un argumento o valor que forma parte de la directiva) debe ir precedido del delimitador de comentario de una sola línea (//) o incluirse entre delimitadores de comentario (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="f51e4-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="f51e4-128">Las líneas que contienen directivas de preprocesador se pueden continuar inmediatamente antes del marcador de fin de línea con una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="f51e4-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\\).</span></span>

<span data-ttu-id="f51e4-129">Las directivas de preprocesador pueden aparecer en cualquier lugar de un archivo de código fuente, pero solo se aplican al resto del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="f51e4-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f51e4-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f51e4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f51e4-131">Apéndice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f51e4-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




