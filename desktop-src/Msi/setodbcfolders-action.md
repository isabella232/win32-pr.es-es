---
description: La acción SetODBCFolders comprueba los controladores ODBC existentes en el sistema y establece el directorio de destino de cada nuevo controlador en la ubicación de un controlador existente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Acción SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677303"
---
# <a name="setodbcfolders-action"></a><span data-ttu-id="17f50-103">Acción SetODBCFolders</span><span class="sxs-lookup"><span data-stu-id="17f50-103">SetODBCFolders Action</span></span>

<span data-ttu-id="17f50-104">La acción SetODBCFolders comprueba los controladores ODBC existentes en el sistema y establece el directorio de destino de cada nuevo controlador en la ubicación de un controlador existente.</span><span class="sxs-lookup"><span data-stu-id="17f50-104">The SetODBCFolders action checks for existing ODBC drivers on the system and sets the target directory of each new driver to the location of an existing driver.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="17f50-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="17f50-105">Sequence Restrictions</span></span>

<span data-ttu-id="17f50-106">La acción SetODBCFolders debe aparecer después de la [acción CostFinalize](costfinalize-action.md) y antes de la [acción InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="17f50-106">The SetODBCFolders action must come after the [CostFinalize action](costfinalize-action.md) and before the [InstallValidate action](installvalidate-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="17f50-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="17f50-107">ActionData Messages</span></span>



| <span data-ttu-id="17f50-108">Campo</span><span class="sxs-lookup"><span data-stu-id="17f50-108">Field</span></span> | <span data-ttu-id="17f50-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="17f50-109">Description of action data</span></span>                                                          |
|-------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17f50-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="17f50-110">\[1\]</span></span> | <span data-ttu-id="17f50-111">Descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="17f50-111">Driver description.</span></span> <span data-ttu-id="17f50-112">La clave del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="17f50-112">The ODBC driver key.</span></span>                                            |
| <span data-ttu-id="17f50-113">\[2\]</span><span class="sxs-lookup"><span data-stu-id="17f50-113">\[2\]</span></span> | <span data-ttu-id="17f50-114">Ubicación de la carpeta original del nuevo controlador.</span><span class="sxs-lookup"><span data-stu-id="17f50-114">Original folder location of the new driver.</span></span>                                         |
| <span data-ttu-id="17f50-115">\[3\]</span><span class="sxs-lookup"><span data-stu-id="17f50-115">\[3\]</span></span> | <span data-ttu-id="17f50-116">Nueva ubicación de la carpeta para el nuevo controlador.</span><span class="sxs-lookup"><span data-stu-id="17f50-116">New folder location for the new driver.</span></span> <span data-ttu-id="17f50-117">Esta es la ubicación de un controlador existente.</span><span class="sxs-lookup"><span data-stu-id="17f50-117">This is the location of an existing driver.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="17f50-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17f50-118">Remarks</span></span>

<span data-ttu-id="17f50-119">Esta acción coloca un nuevo controlador en el mismo directorio que el controlador existente que se está reemplazando.</span><span class="sxs-lookup"><span data-stu-id="17f50-119">This action places a new driver into the same directory as the existing driver being replaced.</span></span> <span data-ttu-id="17f50-120">La acción SetODBCFolders utiliza la [tabla del directorio](directory-table.md) para establecer las ubicaciones de los controladores existentes que se van a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="17f50-120">The SetODBCFolders action uses the [Directory table](directory-table.md) to set the locations of existing drivers that are to be replaced.</span></span>

 

 



