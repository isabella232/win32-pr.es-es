---
description: Si se establece este bit, el cuadro de diálogo llama periódicamente al instalador.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit de estilo del cuadro de diálogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153742"
---
# <a name="trackdiskspace-dialog-style-bit"></a><span data-ttu-id="43ef0-103">Bit de estilo del cuadro de diálogo TrackDiskSpace</span><span class="sxs-lookup"><span data-stu-id="43ef0-103">TrackDiskSpace Dialog Style Bit</span></span>

<span data-ttu-id="43ef0-104">Si se establece este bit, el cuadro de diálogo llama periódicamente al instalador.</span><span class="sxs-lookup"><span data-stu-id="43ef0-104">If this bit is set, the dialog box periodically calls the installer.</span></span> <span data-ttu-id="43ef0-105">Si la propiedad cambia, notifica a los controles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="43ef0-105">If the property changes, it notifies the controls on the dialog.</span></span> <span data-ttu-id="43ef0-106">Este estilo se puede usar si hay un control en el cuadro de diálogo que indica el espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="43ef0-106">This style can be used if there is a control on the dialog indicating disk space.</span></span> <span data-ttu-id="43ef0-107">Si el usuario cambia a otra aplicación, agrega o quita archivos o modifica el espacio en disco disponible, puede implementar rápidamente el cambio con este estilo.</span><span class="sxs-lookup"><span data-stu-id="43ef0-107">If the user switches to another application, adds or removes files, or otherwise modifies available disk space, you can quickly implement the change using this style.</span></span>

<span data-ttu-id="43ef0-108">Cualquier cuadro de diálogo que dependa de la propiedad [**OutOfDiskSpace**](outofdiskspace.md) para determinar si se debe mostrar un cuadro de diálogo debe establecer el bit de estilo de cuadro de diálogo TrackDiskSpace del cuadro de diálogo para actualizar dinámicamente el espacio en los volúmenes de destino.</span><span class="sxs-lookup"><span data-stu-id="43ef0-108">Any dialog box relying on the [**OutOfDiskSpace**](outofdiskspace.md) property to determine whether to bring up a dialog must set the TrackDiskSpace Dialog Style Bit for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="value"></a><span data-ttu-id="43ef0-109">Value</span><span class="sxs-lookup"><span data-stu-id="43ef0-109">Value</span></span>



| <span data-ttu-id="43ef0-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="43ef0-110">Decimal</span></span> | <span data-ttu-id="43ef0-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="43ef0-111">Hexadecimal</span></span> | <span data-ttu-id="43ef0-112">Constante</span><span class="sxs-lookup"><span data-stu-id="43ef0-112">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="43ef0-113">32</span><span class="sxs-lookup"><span data-stu-id="43ef0-113">32</span></span>      | <span data-ttu-id="43ef0-114">0x00000020</span><span class="sxs-lookup"><span data-stu-id="43ef0-114">0x00000020</span></span>  | <span data-ttu-id="43ef0-115">**msidbDialogAttributesTrackDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="43ef0-115">**msidbDialogAttributesTrackDiskSpace**</span></span> |



 

 

 



