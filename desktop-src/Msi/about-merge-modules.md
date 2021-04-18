---
description: Los módulos de combinación son esencialmente archivos. msi simplificados, que es la extensión de nombre de archivo de un paquete de instalación de Windows Installer. Un módulo de combinación estándar tiene una extensión de nombre de archivo. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Acerca de los módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360633"
---
# <a name="about-merge-modules"></a><span data-ttu-id="7b75e-104">Acerca de los módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="7b75e-104">About Merge Modules</span></span>

<span data-ttu-id="7b75e-105">Los módulos de combinación son esencialmente archivos. msi simplificados, que es la extensión de nombre de archivo de un paquete de instalación de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7b75e-105">Merge modules are essentially simplified .msi files, which is the file name extension for a Windows Installer installation package.</span></span> <span data-ttu-id="7b75e-106">Un módulo de combinación estándar tiene una extensión de nombre de archivo. msm.</span><span class="sxs-lookup"><span data-stu-id="7b75e-106">A standard merge module has an .msm file name extension.</span></span>

<span data-ttu-id="7b75e-107">Un módulo de combinación no se puede instalar por sí solo porque carece de algunas tablas de base de datos vitales que se encuentran en una base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="7b75e-107">A merge module cannot be installed alone because its lacks some vital database tables that are present in an installation database.</span></span> <span data-ttu-id="7b75e-108">Los módulos de combinación también contienen tablas adicionales que son únicas de sí mismos.</span><span class="sxs-lookup"><span data-stu-id="7b75e-108">Merge modules also contain additional tables that are unique to themselves.</span></span> <span data-ttu-id="7b75e-109">Para instalar la información proporcionada por un módulo de combinación con una aplicación, primero se debe mezclar el módulo en el archivo. msi de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7b75e-109">To install the information delivered by a merge module with an application, the module must first be merged into the application's .msi file.</span></span>

<span data-ttu-id="7b75e-110">Un módulo de combinación consta de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="7b75e-110">A merge module consists of the following parts:</span></span>

-   <span data-ttu-id="7b75e-111">[Base de datos de módulo de mezcla](merge-module-database.md) que contiene las propiedades de instalación y la lógica de configuración que entrega el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="7b75e-111">A [Merge Module Database](merge-module-database.md) containing the installation properties and setup logic being delivered by the merge module.</span></span>
-   <span data-ttu-id="7b75e-112">Referencia de la [secuencia de información de resumen del módulo de combinación que](merge-module-summary-information-stream-reference.md) describe el módulo.</span><span class="sxs-lookup"><span data-stu-id="7b75e-112">A [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md) describing the module.</span></span>
-   <span data-ttu-id="7b75e-113">Un archivo. cab de [MergeModule.CABinet](mergemodule-cabinet.md) almacenado como una secuencia dentro del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="7b75e-113">A [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file stored as a stream inside the merge module.</span></span> <span data-ttu-id="7b75e-114">Este archivo. cab contiene todos los archivos necesarios para los componentes que entrega el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="7b75e-114">This cabinet contains all the files required by the components delivered by the merge module.</span></span>

<span data-ttu-id="7b75e-115">[Varios módulos de combinación de lenguajes](multiple-language-merge-modules.md) pueden proporcionar componentes a un paquete de instalación en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="7b75e-115">[Multiple language merge modules](multiple-language-merge-modules.md) can deliver components to an installation package in multiple languages.</span></span> <span data-ttu-id="7b75e-116">En un módulo de combinación de varios idiomas, la base de datos contiene las propiedades de instalación y la lógica para más de un idioma y el MergeModule.CABarchivo. cab de inet incluye todos los archivos necesarios para instalar componentes con todos los idiomas admitidos por el módulo.</span><span class="sxs-lookup"><span data-stu-id="7b75e-116">In a multiple language merge module the database contains the installation properties and logic for more than one language and the MergeModule.CABinet cabinet includes all the files necessary to install components with all the languages supported by the module.</span></span>

 

 



