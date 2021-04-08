---
description: No se puede tener acceso a una sesión del instalador desde una acción personalizada que no sea la sesión de instalación actual.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Obtener acceso a una base de datos o una sesión desde una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001771"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a><span data-ttu-id="b1877-103">Obtener acceso a una base de datos o una sesión desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="b1877-103">Accessing a Database or Session from Inside a Custom Action</span></span>

<span data-ttu-id="b1877-104">No se puede tener acceso a una sesión del instalador desde una acción personalizada que no sea la sesión de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="b1877-104">You cannot access an installer session from a custom action that is not the current installation session.</span></span> <span data-ttu-id="b1877-105">Las acciones personalizadas se limitan a trabajar solo con la base de datos activa de la sesión y ninguna otra base de datos.</span><span class="sxs-lookup"><span data-stu-id="b1877-105">Custom actions are limited to working with only the active database of the session and no other databases.</span></span> <span data-ttu-id="b1877-106">No se debe llamar a las siguientes [funciones de base de datos](database-functions.md) de Windows Installer desde una acción personalizada, ya que requieren un identificador a una base de datos que no sea la base de datos de la sesión de instalación actual:</span><span class="sxs-lookup"><span data-stu-id="b1877-106">The following Windows Installer [Database Functions](database-functions.md) must not be called from a custom action, because they require a handle to a database that is not the database of the current installation session:</span></span>

[<span data-ttu-id="b1877-107">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="b1877-107">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[<span data-ttu-id="b1877-108">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="b1877-108">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[<span data-ttu-id="b1877-109">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="b1877-109">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[<span data-ttu-id="b1877-110">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="b1877-110">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[<span data-ttu-id="b1877-111">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="b1877-111">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[<span data-ttu-id="b1877-112">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="b1877-112">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[<span data-ttu-id="b1877-113">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="b1877-113">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[<span data-ttu-id="b1877-114">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="b1877-114">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[<span data-ttu-id="b1877-115">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="b1877-115">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a><span data-ttu-id="b1877-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1877-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1877-117">Obtener acceso a la sesión del instalador actual desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="b1877-117">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



