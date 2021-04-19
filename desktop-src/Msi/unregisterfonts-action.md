---
description: La acción UnregisterFonts quita del sistema la información de registro sobre las fuentes instaladas.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Acción UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678524"
---
# <a name="unregisterfonts-action"></a><span data-ttu-id="9dcc2-103">Acción UnregisterFonts</span><span class="sxs-lookup"><span data-stu-id="9dcc2-103">UnregisterFonts Action</span></span>

<span data-ttu-id="9dcc2-104">La acción UnregisterFonts quita del sistema la información de registro sobre las fuentes instaladas.</span><span class="sxs-lookup"><span data-stu-id="9dcc2-104">The UnregisterFonts action removes registration information about installed fonts from the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9dcc2-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="9dcc2-105">Sequence Restrictions</span></span>

<span data-ttu-id="9dcc2-106">Se debe llamar a la acción [RemoveFiles](removefiles-action.md) después de UnregisterFonts.</span><span class="sxs-lookup"><span data-stu-id="9dcc2-106">The [RemoveFiles](removefiles-action.md) action must be called after UnregisterFonts.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9dcc2-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="9dcc2-107">ActionData Messages</span></span>



| <span data-ttu-id="9dcc2-108">Campo</span><span class="sxs-lookup"><span data-stu-id="9dcc2-108">Field</span></span> | <span data-ttu-id="9dcc2-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="9dcc2-109">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="9dcc2-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9dcc2-110">\[1\]</span></span> | <span data-ttu-id="9dcc2-111">Archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="9dcc2-111">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="9dcc2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dcc2-112">Remarks</span></span>

<span data-ttu-id="9dcc2-113">La acción UnregisterFonts se ejecuta si el archivo especificado en la \_ columna de archivo de la [tabla de fuentes](font-table.md) pertenece a un componente que se va a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="9dcc2-113">The UnregisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being uninstalled.</span></span>

 

 



