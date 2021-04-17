---
description: Los componentes indican el orden de los datos que representan a través de un tipo.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Tipos de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697790"
---
# <a name="component-types"></a><span data-ttu-id="7195a-103">Tipos de componentes</span><span class="sxs-lookup"><span data-stu-id="7195a-103">Component Types</span></span>

<span data-ttu-id="7195a-104">Los componentes indican el orden de los datos que representan a través de un tipo.</span><span class="sxs-lookup"><span data-stu-id="7195a-104">Components indicate the sort of data they represent through a type.</span></span>

<span data-ttu-id="7195a-105">Actualmente, los tipos de componentes (vea [**\_ \_ tipo de componente de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) se limitan a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7195a-105">Currently, component types (see [**VSS\_COMPONENT\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) are limited to the following:</span></span>

-   <span data-ttu-id="7195a-106">Componentes de base de datos</span><span class="sxs-lookup"><span data-stu-id="7195a-106">Database components</span></span>
-   <span data-ttu-id="7195a-107">Grupos de archivos</span><span class="sxs-lookup"><span data-stu-id="7195a-107">File groups</span></span>

<span data-ttu-id="7195a-108">Para obtener información sobre la implementación de la configuración [de los tipos de componentes, consulte definición de componentes por escritores](definition-of-components-by-writers.md).</span><span class="sxs-lookup"><span data-stu-id="7195a-108">For implementation information about setting component types, see [Definition of Components by Writers](definition-of-components-by-writers.md).</span></span>

<span data-ttu-id="7195a-109">Los escritores tienen un tipo de datos que indica su uso (consulte [**\_ \_ tipo de origen de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), que puede ser el siguiente:</span><span class="sxs-lookup"><span data-stu-id="7195a-109">Writers have a data typing that indicates their usage (see [**VSS\_SOURCE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), which can be the following:</span></span>

-   <span data-ttu-id="7195a-110">Una base de datos transaccional (como un servidor SQL Server)</span><span class="sxs-lookup"><span data-stu-id="7195a-110">A transactional database (such as an SQL server)</span></span>
-   <span data-ttu-id="7195a-111">Una base de datos no transaccional (como un cliente de hoja de cálculo)</span><span class="sxs-lookup"><span data-stu-id="7195a-111">A nontransactional database (such as a spreadsheet client)</span></span>
-   <span data-ttu-id="7195a-112">Grupo de archivos (otro)</span><span class="sxs-lookup"><span data-stu-id="7195a-112">File group (other)</span></span>

<span data-ttu-id="7195a-113">La especificación de un tipo de componente como base de datos permite la identificación más fácil de su contenido, permite el control independiente de los archivos de registro y de datos (vea [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) y [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para obtener más información) y aplica mayor rigor en la selección de archivos al no permitir la selección de archivos recursivos o usar una [*ruta de acceso alternativa*](vssgloss-a.md) (consulte [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) y [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)</span><span class="sxs-lookup"><span data-stu-id="7195a-113">Specifying a component type as database allows for easier identification of its content, allows for separate handling of log and data files (see [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) for details), and enforces greater rigor in file selection by not allowing either recursive file selection or using an [*alternate path*](vssgloss-a.md) (see [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) and [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span></span>

<span data-ttu-id="7195a-114">Por otro lado, con un componente de grupo de archivos, con el precio de no saber qué datos contiene, tiene mayor libertad sobre cómo se insertan los archivos, ya que puede usar una especificación recursiva y rutas de acceso alternativas.</span><span class="sxs-lookup"><span data-stu-id="7195a-114">With a file group component, on the other hand, at the price of not knowing what data it contains, you have greater freedom about how files are inserted, because you can use recursive specification and alternate paths.</span></span>

<span data-ttu-id="7195a-115">Se pueden agregar más tipos de componentes en el futuro.</span><span class="sxs-lookup"><span data-stu-id="7195a-115">Additional component types may be added in the future.</span></span>

 

 



