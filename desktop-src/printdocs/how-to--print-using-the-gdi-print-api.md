---
description: En este tema se presenta cómo imprimir desde un programa de Windows nativo mediante el&GDI \# 160; Imprime&\# 160; API.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Cómo: imprimir mediante la API de impresión de GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913153"
---
# <a name="how-to-print-using-the-gdi-print-api"></a><span data-ttu-id="e8b9e-103">Cómo: imprimir mediante la API de impresión de GDI</span><span class="sxs-lookup"><span data-stu-id="e8b9e-103">How To: Print Using the GDI Print API</span></span>

<span data-ttu-id="e8b9e-104">En este tema se explica cómo imprimir desde un programa nativo de Windows mediante la [API de impresión de GDI](gdi-printing.md).</span><span class="sxs-lookup"><span data-stu-id="e8b9e-104">This topic introduces how to print from a native Windows program using the [GDI Print API](gdi-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="e8b9e-105">Información general</span><span class="sxs-lookup"><span data-stu-id="e8b9e-105">Overview</span></span>

<span data-ttu-id="e8b9e-106">La impresión suele ser una parte integral de un programa de Windows nativo, por lo que no es una característica que se puede agregar fácilmente después de haber escrito el programa.</span><span class="sxs-lookup"><span data-stu-id="e8b9e-106">Printing is usually an integral part of a native Windows program, so it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="e8b9e-107">Al diseñar un programa para Windows 7, debería considerar la posibilidad de usar la [API de impresión XPS](xps-printing.md) para proporcionar la funcionalidad de impresión porque proporciona la máxima compatibilidad para el futuro.</span><span class="sxs-lookup"><span data-stu-id="e8b9e-107">When designing a program for Windows 7, you should consider using the [XPS Print API](xps-printing.md) to provide the printing functionality because it provides the most compatibility for the future.</span></span> <span data-ttu-id="e8b9e-108">Es más probable que los programas que se deben ejecutar en Windows Vista y versiones anteriores de Windows usen la [API de impresión GDI](gdi-printing.md) para proporcionar la funcionalidad de impresión.</span><span class="sxs-lookup"><span data-stu-id="e8b9e-108">Programs that must run on Windows Vista and earlier versions of Windows will most likely use the [GDI Print API](gdi-printing.md) to provide printing functionality.</span></span> <span data-ttu-id="e8b9e-109">La API de impresión GDI también se admite en Windows 7, pero es más limitada que la API de impresión XPS.</span><span class="sxs-lookup"><span data-stu-id="e8b9e-109">The GDI Print API is also supported in Windows 7, but it is more limited than the XPS Print API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8b9e-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8b9e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8b9e-111">Usar la impresión</span><span class="sxs-lookup"><span data-stu-id="e8b9e-111">Using Printing</span></span>](using-printing.md)
</dt> <dt>

[<span data-ttu-id="e8b9e-112">Cómo imprimir desde una aplicación de Windows</span><span class="sxs-lookup"><span data-stu-id="e8b9e-112">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



