---
description: La acción InstallAdminPackage copia la base de datos del producto en el punto de instalación administrativa, que se define mediante la propiedad TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Acción InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001710"
---
# <a name="installadminpackage-action"></a><span data-ttu-id="03d5c-103">Acción InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="03d5c-103">InstallAdminPackage Action</span></span>

<span data-ttu-id="03d5c-104">La acción InstallAdminPackage copia la base de datos del producto en el punto de instalación administrativa, que se define mediante la propiedad [**targetDir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="03d5c-104">The InstallAdminPackage action copies the product database to the administrative installation point, which is defined by the [**TARGETDIR**](targetdir.md) property.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="03d5c-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="03d5c-105">Sequence Restrictions</span></span>

<span data-ttu-id="03d5c-106">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="03d5c-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="03d5c-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="03d5c-107">ActionData Messages</span></span>



| <span data-ttu-id="03d5c-108">Campo</span><span class="sxs-lookup"><span data-stu-id="03d5c-108">Field</span></span> | <span data-ttu-id="03d5c-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="03d5c-109">Description of action data</span></span>                                 |
|-------|------------------------------------------------------------|
| <span data-ttu-id="03d5c-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="03d5c-110">\[1\]</span></span> | <span data-ttu-id="03d5c-111">Nombre de los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="03d5c-111">Name of install files.</span></span>                                     |
| <span data-ttu-id="03d5c-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="03d5c-112">\[6\]</span></span> | <span data-ttu-id="03d5c-113">Tamaño de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="03d5c-113">Size of database.</span></span>                                          |
| <span data-ttu-id="03d5c-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="03d5c-114">\[9\]</span></span> | <span data-ttu-id="03d5c-115">Identificador de instalación administrativa: directorio de puntos.</span><span class="sxs-lookup"><span data-stu-id="03d5c-115">Identifier of administrative installation–point directory.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="03d5c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03d5c-116">Remarks</span></span>

<span data-ttu-id="03d5c-117">La acción InstallAdminPackage también actualiza la información de Resumen de la base de datos y quita los archivos. cab que se encuentran en los flujos una vez copiada la base de datos.</span><span class="sxs-lookup"><span data-stu-id="03d5c-117">The InstallAdminPackage action also updates the summary information of the database and removes any cabinet files located in streams after the database is copied.</span></span>

 

 



