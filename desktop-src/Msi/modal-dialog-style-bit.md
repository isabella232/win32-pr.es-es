---
description: Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros cuadros de diálogo de la misma aplicación y el cuadro de diálogo mantiene el control mientras se está ejecutando.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de estilo del cuadro de diálogo modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546358"
---
# <a name="modal-dialog-style-bit"></a><span data-ttu-id="f0758-103">Bit de estilo del cuadro de diálogo modal</span><span class="sxs-lookup"><span data-stu-id="f0758-103">Modal Dialog Style Bit</span></span>

<span data-ttu-id="f0758-104">Si se establece este bit, el cuadro de diálogo es modal, no se pueden colocar otros cuadros de diálogo de la misma aplicación y el cuadro de diálogo mantiene el control mientras se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f0758-104">If this bit is set, the dialog box is modal, other dialogs of the same application cannot be put on top of it, and the dialog keeps the control while it is running.</span></span> <span data-ttu-id="f0758-105">Si no se establece este bit, el cuadro de diálogo es un modelo no modal; puede que otros cuadros de diálogo de la misma aplicación se muevan por encima.</span><span class="sxs-lookup"><span data-stu-id="f0758-105">If this bit is not set, the dialog is modeless, other dialogs of the same application may be moved on top of it.</span></span> <span data-ttu-id="f0758-106">Después de crear y mostrar un cuadro de diálogo no modal, la interfaz de usuario devuelve el control al instalador.</span><span class="sxs-lookup"><span data-stu-id="f0758-106">After a modeless dialog is created and displayed, the user interface returns control to the installer.</span></span> <span data-ttu-id="f0758-107">Después, el instalador llama a la interfaz de usuario periódicamente para actualizar el cuadro de diálogo y darle la oportunidad de procesar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f0758-107">The installer then calls the user interface periodically to update the dialog and to give it a chance to process the messages.</span></span> <span data-ttu-id="f0758-108">En cuanto esto se hace, el control se devuelve al instalador.</span><span class="sxs-lookup"><span data-stu-id="f0758-108">As soon as this is done, the control is returned to the installer.</span></span>

> [!Note]  
> <span data-ttu-id="f0758-109">No debería haber ningún cuadro de diálogo no modal en una secuencia del asistente, ya que esto devolvería el control al instalador, finalizando la secuencia del asistente prematuramente.</span><span class="sxs-lookup"><span data-stu-id="f0758-109">There should be no modeless dialogs in a wizard sequence, since this would return control to the installer, ending the wizard sequence prematurely.</span></span>

 

## <a name="value"></a><span data-ttu-id="f0758-110">Value</span><span class="sxs-lookup"><span data-stu-id="f0758-110">Value</span></span>



| <span data-ttu-id="f0758-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="f0758-111">Decimal</span></span> | <span data-ttu-id="f0758-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f0758-112">Hexadecimal</span></span> | <span data-ttu-id="f0758-113">Constante</span><span class="sxs-lookup"><span data-stu-id="f0758-113">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="f0758-114">2</span><span class="sxs-lookup"><span data-stu-id="f0758-114">2</span></span>       | <span data-ttu-id="f0758-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f0758-115">0x00000002</span></span>  | <span data-ttu-id="f0758-116">**msidbDialogAttributesSysModal**</span><span class="sxs-lookup"><span data-stu-id="f0758-116">**msidbDialogAttributesSysModal**</span></span> |



 

 

 



