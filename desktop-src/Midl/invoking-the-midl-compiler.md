---
title: Invocar el compilador MIDL
description: El compilador MIDL puede generar código para distintas plataformas y versiones del sistema. Consulte el modificador/Target para obtener más información acerca de los modificadores sugeridos y cómo generar código optimizado para una versión determinada.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL del compilador MIDL, invocar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2019
ms.locfileid: "105651324"
---
# <a name="invoking-the-midl-compiler"></a><span data-ttu-id="21404-105">Invocar el compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="21404-105">Invoking the MIDL Compiler</span></span>

<span data-ttu-id="21404-106">El compilador MIDL puede generar código para distintas plataformas y versiones del sistema.</span><span class="sxs-lookup"><span data-stu-id="21404-106">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="21404-107">Consulte el modificador [**/target**](-target.md) para obtener más información acerca de los modificadores sugeridos y cómo generar código optimizado para una versión determinada.</span><span class="sxs-lookup"><span data-stu-id="21404-107">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a particular release.</span></span>

<span data-ttu-id="21404-108">Ejecute el compilador MIDL desde la línea de comandos con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="21404-108">Run the MIDL compiler from the command line using the following command:</span></span>

<span data-ttu-id="21404-109"> *<  opciones >* de MIDL **filename. idl**</span><span class="sxs-lookup"><span data-stu-id="21404-109">**midl** *<***options***>* **filename.idl**</span></span>

<span data-ttu-id="21404-110">donde *< ***Options*** >* representa las opciones de línea de comandos que desea utilizar y FILENAME. idl es el nombre del archivo MIDL que se va a compilar.</span><span class="sxs-lookup"><span data-stu-id="21404-110">where *<***options***>* represents the command-line options you want to use, and Filename.idl is the name of the MIDL file to compile.</span></span>

<span data-ttu-id="21404-111">Hay disponible una lista completa de las opciones y los modificadores del compilador MIDL cuando se usa el compilador de MIDL [**/Help**](-help-.md) y/?</span><span class="sxs-lookup"><span data-stu-id="21404-111">A complete listing of MIDL compiler switches and options is available when you use the MIDL compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="21404-112">centrales.</span><span class="sxs-lookup"><span data-stu-id="21404-112">switches.</span></span> <span data-ttu-id="21404-113">Los modificadores están organizados por categorías.</span><span class="sxs-lookup"><span data-stu-id="21404-113">The switches are organized by categories.</span></span> <span data-ttu-id="21404-114">Para obtener más información, vea la [referencia de Command-Line de MIDL](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="21404-114">For details, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

> [!NOTE]
> <span data-ttu-id="21404-115">La nueva marca global **$ (optimización de MIDL \_ )** existe en Win32. Mak.</span><span class="sxs-lookup"><span data-stu-id="21404-115">The new global flag **$(MIDL\_OPTIMIZATION)** exists in win32.mak.</span></span> <span data-ttu-id="21404-116">Cuando se compila un archivo. idl con esta marca, el código auxiliar generado puede utilizar las características de RPC más recientes disponibles en la plataforma especificada y, potencialmente, mejorar el rendimiento y la estabilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21404-116">When an .idl file is compiled using this flag, the generated stub can utilize the latest RPC features available on the specified platform, and potentially improve the application's performance and stability.</span></span> <span data-ttu-id="21404-117">Se recomienda que las aplicaciones usen esta marca al usar MIDL.</span><span class="sxs-lookup"><span data-stu-id="21404-117">It's recommended that applications use this flag when using MIDL.</span></span>
>
> <span data-ttu-id="21404-118">**MIDL** **$ (optimización de MIDL \_ )** **...**</span><span class="sxs-lookup"><span data-stu-id="21404-118">**midl** **$(MIDL\_OPTIMIZATION)** **...**</span></span>