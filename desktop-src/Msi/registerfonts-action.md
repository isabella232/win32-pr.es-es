---
description: La acción RegisterFonts registra las fuentes instaladas en el sistema. Esta acción asigna el nombre de la fuente de la columna FontTitle de la tabla fuente a la ruta de acceso del archivo de fuente instalado.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Acción RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652668"
---
# <a name="registerfonts-action"></a><span data-ttu-id="d5842-104">Acción RegisterFonts</span><span class="sxs-lookup"><span data-stu-id="d5842-104">RegisterFonts Action</span></span>

<span data-ttu-id="d5842-105">La acción RegisterFonts registra las fuentes instaladas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d5842-105">The RegisterFonts action registers installed fonts with the system.</span></span> <span data-ttu-id="d5842-106">Esta acción asigna el nombre de la fuente de la columna FontTitle de la [tabla fuente](font-table.md) a la ruta de acceso del archivo de fuente instalado.</span><span class="sxs-lookup"><span data-stu-id="d5842-106">This action maps the font name in the FontTitle column of the [Font table](font-table.md) to the path of the font file installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d5842-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="d5842-107">Sequence Restrictions</span></span>

<span data-ttu-id="d5842-108">Se debe llamar a la acción [InstallFiles](installfiles-action.md) antes de llamar a la acción RegisterFonts.</span><span class="sxs-lookup"><span data-stu-id="d5842-108">The [InstallFiles](installfiles-action.md) action must be called before calling the RegisterFonts action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d5842-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="d5842-109">ActionData Messages</span></span>



| <span data-ttu-id="d5842-110">Campo</span><span class="sxs-lookup"><span data-stu-id="d5842-110">Field</span></span> | <span data-ttu-id="d5842-111">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="d5842-111">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="d5842-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d5842-112">\[1\]</span></span> | <span data-ttu-id="d5842-113">Archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="d5842-113">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="d5842-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5842-114">Remarks</span></span>

<span data-ttu-id="d5842-115">La acción RegisterFonts se ejecuta si el archivo especificado en la \_ columna de archivo de la [tabla de fuentes](font-table.md) pertenece a un componente que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="d5842-115">The RegisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being installed.</span></span>

 

 



