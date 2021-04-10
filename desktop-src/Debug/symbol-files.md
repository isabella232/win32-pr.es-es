---
description: Normalmente, la información de depuración se almacena en un archivo de símbolos independiente del ejecutable.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Archivos de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152847"
---
# <a name="symbol-files"></a><span data-ttu-id="d6f64-103">Archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="d6f64-103">Symbol Files</span></span>

<span data-ttu-id="d6f64-104">Normalmente, la información de depuración se almacena en un archivo de símbolos independiente del ejecutable.</span><span class="sxs-lookup"><span data-stu-id="d6f64-104">Normally, debugging information is stored in a symbol file separate from the executable.</span></span> <span data-ttu-id="d6f64-105">La implementación de esta información de depuración ha cambiado a lo largo de los años y en la siguiente documentación se proporcionan instrucciones sobre estas distintas implementaciones.</span><span class="sxs-lookup"><span data-stu-id="d6f64-105">The implementation of this debugging information has changed over the years, and the following documentation will provide guidance regarding these various implementations.</span></span>

## <a name="pdb-files"></a><span data-ttu-id="d6f64-106">PDB (archivos)</span><span class="sxs-lookup"><span data-stu-id="d6f64-106">PDB files</span></span>

<span data-ttu-id="d6f64-107">Todas las versiones modernas de los compiladores de Microsoft almacenan información de depuración sobre un ejecutable compilado en un archivo de *base de datos de programa* (. pdb) independiente.</span><span class="sxs-lookup"><span data-stu-id="d6f64-107">All modern versions of the Microsoft compilers store debugging information about a compiled executable in a separate *program database* (.pdb) file.</span></span> <span data-ttu-id="d6f64-108">Este archivo se conoce comúnmente como *PDB*.</span><span class="sxs-lookup"><span data-stu-id="d6f64-108">This file is commonly referred to as a *PDB*.</span></span> <span data-ttu-id="d6f64-109">Los datos se almacenan en un archivo independiente del ejecutable para limitar el tamaño del archivo ejecutable, lo que ahorra espacio de almacenamiento en disco y reduce el tiempo necesario para cargar los datos.</span><span class="sxs-lookup"><span data-stu-id="d6f64-109">The data is stored in a separate file from the executable to help limit the size of the executable, saving disk storage space and reducing the time it takes to load the data.</span></span> <span data-ttu-id="d6f64-110">Esta metodología también permite que el ejecutable se distribuya sin revelar esta información importante, lo que podría facilitar el uso del programa de ingeniería inversa.</span><span class="sxs-lookup"><span data-stu-id="d6f64-110">This methodology also allows the executable to be distributed without disclosing this significant information which could make the program easier to reverse engineer.</span></span>

<span data-ttu-id="d6f64-111">Para crear un PDB, compile el archivo ejecutable con la información de depuración de acuerdo con las instrucciones de las herramientas de compilación.</span><span class="sxs-lookup"><span data-stu-id="d6f64-111">To create a PDB, build your executable file with debugging information according to the directions for your build tools.</span></span>

<span data-ttu-id="d6f64-112">La API de DbgHelp puede usar archivos PDB para obtener la información siguiente.</span><span class="sxs-lookup"><span data-stu-id="d6f64-112">The DbgHelp API is able to use PDBs to obtain the following information.</span></span>

-   <span data-ttu-id="d6f64-113">públicos y exportaciones</span><span class="sxs-lookup"><span data-stu-id="d6f64-113">publics and exports</span></span>
-   <span data-ttu-id="d6f64-114">símbolos globales</span><span class="sxs-lookup"><span data-stu-id="d6f64-114">global symbols</span></span>
-   <span data-ttu-id="d6f64-115">símbolos locales</span><span class="sxs-lookup"><span data-stu-id="d6f64-115">local symbols</span></span>
-   <span data-ttu-id="d6f64-116">datos de tipo</span><span class="sxs-lookup"><span data-stu-id="d6f64-116">type data</span></span>
-   <span data-ttu-id="d6f64-117">archivos de código fuente</span><span class="sxs-lookup"><span data-stu-id="d6f64-117">source files</span></span>
-   <span data-ttu-id="d6f64-118">números de línea</span><span class="sxs-lookup"><span data-stu-id="d6f64-118">line numbers</span></span>

## <a name="dbg-files-and-embedded-debug-information"></a><span data-ttu-id="d6f64-119">Archivos DBG e información de depuración incrustada</span><span class="sxs-lookup"><span data-stu-id="d6f64-119">DBG files and embedded debug information</span></span>

<span data-ttu-id="d6f64-120">Las versiones anteriores del conjunto de herramientas de Microsoft usaban para incrustar la información de depuración en el archivo ejecutable, pero normalmente se eliminarían en un archivo independiente con la extensión. dbg.</span><span class="sxs-lookup"><span data-stu-id="d6f64-120">Previous versions of the Microsoft toolset used to embed the debugging information in the executable, however it would normally be stripped out into a separate file with a .dbg extension.</span></span> <span data-ttu-id="d6f64-121">Esto se conoce comúnmente como archivo *dbg* .</span><span class="sxs-lookup"><span data-stu-id="d6f64-121">This is commonly known as a *DBG* file.</span></span> <span data-ttu-id="d6f64-122">Los archivos DBG usan el mismo formato de archivo PE que los ejecutables.</span><span class="sxs-lookup"><span data-stu-id="d6f64-122">DBG files use the same PE file format as executables.</span></span>

<span data-ttu-id="d6f64-123">La compatibilidad con la API de DbgHelp para DBGs y la información de depuración incrustada es limitada e incluye lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d6f64-123">The DbgHelp API support for DBGs and embedded debugging information is limited and includes the following.</span></span>

-   <span data-ttu-id="d6f64-124">públicos y exportaciones</span><span class="sxs-lookup"><span data-stu-id="d6f64-124">publics and exports</span></span>
-   <span data-ttu-id="d6f64-125">símbolos globales</span><span class="sxs-lookup"><span data-stu-id="d6f64-125">global symbols</span></span>

 

 



