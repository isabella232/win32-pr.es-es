---
description: El instalador almacena toda la información sobre la interfaz de usuario en las tablas de la base de datos de instalación.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Obtener una vista previa de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277163"
---
# <a name="previewing-the-user-interface"></a><span data-ttu-id="367a3-103">Obtener una vista previa de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="367a3-103">Previewing the User Interface</span></span>

<span data-ttu-id="367a3-104">El instalador almacena toda la información sobre la [interfaz de usuario](user-interface.md) en las tablas de la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="367a3-104">The installer stores all information about the [user interface](user-interface.md) in the tables of the installation database.</span></span> <span data-ttu-id="367a3-105">Para facilitar el diseño de la interfaz de usuario, el instalador también proporciona un modo de vista previa para ver esta información.</span><span class="sxs-lookup"><span data-stu-id="367a3-105">To facilitate the design of the UI the installer also provides a preview mode for viewing this information.</span></span> <span data-ttu-id="367a3-106">En el procedimiento siguiente se describe cómo habilitar el modo de vista previa de la interfaz de usuario y mostrar la apariencia actual de cuadros de diálogo y cartelera.</span><span class="sxs-lookup"><span data-stu-id="367a3-106">The following procedure describes how to enable the UI preview mode and display the current appearance of dialog boxes and billboards.</span></span>

<span data-ttu-id="367a3-107">**Para ver la interfaz de usuario en el modo de vista previa**</span><span class="sxs-lookup"><span data-stu-id="367a3-107">**To view the user interface in the preview mode**</span></span>

1.  <span data-ttu-id="367a3-108">Habilite el modo de vista previa mediante una llamada a la función [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .</span><span class="sxs-lookup"><span data-stu-id="367a3-108">Enable the preview mode by calling the [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) function.</span></span>
2.  <span data-ttu-id="367a3-109">Para mostrar los cuadros de diálogo concretos, llame a la función [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .</span><span class="sxs-lookup"><span data-stu-id="367a3-109">Display the particular dialog boxes by calling the [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) function.</span></span>
3.  <span data-ttu-id="367a3-110">Mostrar una cartelera determinada mediante una llamada a la función [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .</span><span class="sxs-lookup"><span data-stu-id="367a3-110">Display particular billboards by calling the [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) function.</span></span>

 

 



