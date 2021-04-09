---
description: ICE83 valida la tabla MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082537"
---
# <a name="ice83"></a><span data-ttu-id="ae5c3-103">ICE83</span><span class="sxs-lookup"><span data-stu-id="ae5c3-103">ICE83</span></span>

<span data-ttu-id="ae5c3-104">ICE83 valida la [tabla MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae5c3-104">ICE83 validates the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="ae5c3-105">Esta acción personalizada de ICE publica un error si la ruta de acceso de la clave de un componente que contiene un ensamblado Win32 se establece en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-105">This ICE custom action posts an error if the key path for a component containing a Win32 assembly is set to the manifest file.</span></span> <span data-ttu-id="ae5c3-106">Explícitamente, el error se expone si el valor especificado en el campo de ruta de acceso de la [tabla de componentes](component-table.md) es igual al valor especificado en el \_ campo manifiesto de archivo de la tabla MsiAssembly.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-106">Explicitly the error is posted if the value entered in the KeyPath field of the [Component table](component-table.md) equals the value entered in the File\_Manifest field of the MsiAssembly table.</span></span> <span data-ttu-id="ae5c3-107">Esta acción personalizada de ICE publica un error si hay al menos un registro en la tabla MsiAssembly y la [tabla InstallExecuteSequence](installexecutesequence-table.md) no contiene la [acción MsiPublishAssemblies](msipublishassemblies-action.md) y la [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="ae5c3-107">This ICE custom action posts an error if there is at least one record in the MsiAssembly table and the [InstallExecuteSequence table](installexecutesequence-table.md) does not contain both the [MsiPublishAssemblies Action](msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

## <a name="result"></a><span data-ttu-id="ae5c3-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="ae5c3-108">Result</span></span>

<span data-ttu-id="ae5c3-109">ICE83 expone los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-109">ICE83 posts the following errors.</span></span>



| <span data-ttu-id="ae5c3-110">Error ICE83</span><span class="sxs-lookup"><span data-stu-id="ae5c3-110">ICE83 error</span></span>                                                                                                   | <span data-ttu-id="ae5c3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae5c3-111">Description</span></span>                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5c3-112">La ruta de acceso de la clave para el ensamblado SxS Win32 (componente \_ = \[ 1 \] ) no debe ser su archivo de manifiesto</span><span class="sxs-lookup"><span data-stu-id="ae5c3-112">The key path for Win32 SXS Assembly (Component\_=\[1\]) SHOULD NOT be its manifest file</span></span>                       | <span data-ttu-id="ae5c3-113">ICE83 envía este error cuando el campo de ruta de acceso de un ensamblado de Win32 se establece en su archivo de manifiesto (Component. ruta de acceso = = MsiAssembly. file \_ manifest).</span><span class="sxs-lookup"><span data-stu-id="ae5c3-113">ICE83 posts this error when the KeyPath field for a Win32 Assembly is set to its manifest file (Component.KeyPath == MsiAssembly.File\_Manifest).</span></span> <span data-ttu-id="ae5c3-114">\[1 \] es la ruta de rutas en la tabla de componentes</span><span class="sxs-lookup"><span data-stu-id="ae5c3-114">\[1\] is KeyPath in Component table</span></span>                          |
| <span data-ttu-id="ae5c3-115">Las acciones MsiPublishAssemblies y MsiUnpublishAssemblies deben estar presentes en la tabla InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-115">Both MsiPublishAssemblies AND MsiUnpublishAssemblies actions MUST be present in InstallExecuteSequence table.</span></span> | <span data-ttu-id="ae5c3-116">ICE83 envía este error cuando hay al menos una entrada en la tabla MsiAssembly, pero la tabla InstallExecuteSequence no contiene la acción MsiAssemblyPublish y la acción MsiAssemblyUnpublish.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-116">ICE83 posts this error when there is at least one entry in the MsiAssembly table but the InstallExecuteSequence table does not contain both the MsiAssemblyPublish action and the MsiAssemblyUnpublish action.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ae5c3-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae5c3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae5c3-118">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="ae5c3-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



