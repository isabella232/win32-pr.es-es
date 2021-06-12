---
description: Obtenga información sobre Windows Installer conceptos que comienzan por la letra D, como la función de base de datos y la revisión diferencial.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d76378d636c8ae14acdc9cb882c31840e3f1550f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010938"
---
# <a name="d-windows-installer"></a><span data-ttu-id="a7944-103">D (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="a7944-103">D (Windows Installer)</span></span>

<span data-ttu-id="a7944-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L M [N](m-gly.md) [O](o-gly.md) P [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="a7944-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a7944-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**función de base de datos**</span><span class="sxs-lookup"><span data-stu-id="a7944-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="a7944-106">Accede a la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="a7944-106">Accesses the installer database.</span></span> <span data-ttu-id="a7944-107">Estas funciones se proporcionan principalmente [](i-gly.md) para su uso por las herramientas de creación de paquetes del instalador y no están diseñadas para usarse para llamar a los servicios del instalador.</span><span class="sxs-lookup"><span data-stu-id="a7944-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="a7944-108">Para obtener más información, vea [Funciones de base de datos](database-functions.md) y la Referencia de función del [instalador](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a7944-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7944-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**identificador de base de datos**</span><span class="sxs-lookup"><span data-stu-id="a7944-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="a7944-110">Necesario para trabajar con una base de datos.</span><span class="sxs-lookup"><span data-stu-id="a7944-110">Required for working with a database.</span></span> <span data-ttu-id="a7944-111">Para obtener más información, vea [Obtener un identificador de base de datos](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="a7944-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7944-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**revisión delta**</span><span class="sxs-lookup"><span data-stu-id="a7944-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="a7944-113">Una revisión diferencial es una revisión de Windows Installer compresión diferencial creada mediante una herramienta, como Patchwiz.dll, que admite la compresión diferencial.</span><span class="sxs-lookup"><span data-stu-id="a7944-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="a7944-114">Las revisiones que usan la compresión diferencial pueden reducir el tamaño de una actualización proporcionando solo las diferencias (deltas) entre los archivos existentes en un equipo de destino y los nuevos archivos deseados.</span><span class="sxs-lookup"><span data-stu-id="a7944-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="a7944-115">Los nuevos archivos deseados se sintetizan a partir de los archivos existentes y las diferencias descargadas.</span><span class="sxs-lookup"><span data-stu-id="a7944-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="a7944-116">Para obtener más información sobre la tecnología de compresión diferencial, vea La interfaz de programación [de aplicaciones de compresión diferencial](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7944-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



