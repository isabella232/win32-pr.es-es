---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810388"
---
# <a name="d-windows-installer"></a><span data-ttu-id="88c73-103">D (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="88c73-103">D (Windows Installer)</span></span>

<span data-ttu-id="88c73-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [o](o-gly.md) [p](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="88c73-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="88c73-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**función de base de datos**</span><span class="sxs-lookup"><span data-stu-id="88c73-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="88c73-106">Obtiene acceso a la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="88c73-106">Accesses the installer database.</span></span> <span data-ttu-id="88c73-107">Estas funciones se proporcionan principalmente para su uso por parte de [*las herramientas de creación de paquetes del instalador*](i-gly.md) y no están pensadas para usarse para llamar a los servicios del instalador.</span><span class="sxs-lookup"><span data-stu-id="88c73-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="88c73-108">Para obtener más información, vea [funciones de base de datos](database-functions.md) y la referencia de la función de [instalador](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="88c73-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="88c73-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**identificador de base de datos**</span><span class="sxs-lookup"><span data-stu-id="88c73-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="88c73-110">Se requiere para trabajar con una base de datos.</span><span class="sxs-lookup"><span data-stu-id="88c73-110">Required for working with a database.</span></span> <span data-ttu-id="88c73-111">Para obtener más información, vea [obtener un identificador de base de datos](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="88c73-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="88c73-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**revisión diferencial**</span><span class="sxs-lookup"><span data-stu-id="88c73-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="88c73-113">Una revisión diferencial es una revisión de Windows Installer con compresión Delta creada mediante una herramienta, como Patchwiz.dll, que admite la compresión Delta.</span><span class="sxs-lookup"><span data-stu-id="88c73-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="88c73-114">Las revisiones que usan la compresión Delta pueden reducir el tamaño de una actualización proporcionando solo las diferencias (deltas) entre los archivos existentes en un equipo de destino y los nuevos archivos deseados.</span><span class="sxs-lookup"><span data-stu-id="88c73-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="88c73-115">Los archivos nuevos deseados se sintetizan a partir de los archivos existentes y de las diferencias descargadas.</span><span class="sxs-lookup"><span data-stu-id="88c73-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="88c73-116">Para obtener más información acerca de la tecnología de compresión Delta, consulte la [interfaz de programación de aplicaciones de compresión Delta](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="88c73-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



