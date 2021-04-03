---
description: En el procedimiento siguiente se describe un escenario para generar una transformación que oculta una característica de forma permanente.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generar una transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082931"
---
# <a name="generating-a-transform"></a><span data-ttu-id="98b4f-103">Generar una transformación</span><span class="sxs-lookup"><span data-stu-id="98b4f-103">Generating a Transform</span></span>

<span data-ttu-id="98b4f-104">En el procedimiento siguiente se describe un escenario para generar una transformación que oculta una característica de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="98b4f-104">The following procedure describes a scenario to generate a transform that permanently hides a feature.</span></span>

<span data-ttu-id="98b4f-105">**Para ocultar permanentemente una característica del producto**</span><span class="sxs-lookup"><span data-stu-id="98b4f-105">**To permanently hide a product feature**</span></span>

1.  <span data-ttu-id="98b4f-106">Copie el paquete de instalación original.</span><span class="sxs-lookup"><span data-stu-id="98b4f-106">Copy the original installation package.</span></span>
2.  <span data-ttu-id="98b4f-107">Modifique la copia estableciendo el valor de la columna de visualización de la [tabla de características](feature-table.md) en cero.</span><span class="sxs-lookup"><span data-stu-id="98b4f-107">Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero.</span></span> <span data-ttu-id="98b4f-108">Esto especifica ocultar la característica.</span><span class="sxs-lookup"><span data-stu-id="98b4f-108">This specifies hiding the feature.</span></span>
3.  <span data-ttu-id="98b4f-109">Cree una transformación desde el paquete de instalación original a los nuevos paquetes de instalación mediante una llamada a [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span><span class="sxs-lookup"><span data-stu-id="98b4f-109">Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span></span>
4.  <span data-ttu-id="98b4f-110">Cree la información de resumen en la transformación mediante una llamada a [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="98b4f-110">Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

<span data-ttu-id="98b4f-111">La transformación está lista para aplicarse durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="98b4f-111">The transform is then ready to be applied during installation.</span></span> <span data-ttu-id="98b4f-112">Para obtener más información, vea [aplicar transformaciones](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="98b4f-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



