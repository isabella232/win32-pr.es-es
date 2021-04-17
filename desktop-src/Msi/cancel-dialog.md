---
description: Un cuadro de diálogo cancelar confirma que el usuario desea finalizar la instalación. Este es un cuadro de diálogo modal.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Cuadro de diálogo cancelar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652597"
---
# <a name="cancel-dialog"></a><span data-ttu-id="11484-104">Cuadro de diálogo cancelar</span><span class="sxs-lookup"><span data-stu-id="11484-104">Cancel Dialog</span></span>

<span data-ttu-id="11484-105">Un cuadro de diálogo **Cancelar** confirma que el usuario desea finalizar la instalación.</span><span class="sxs-lookup"><span data-stu-id="11484-105">A **Cancel** dialog box confirms that the user wants to terminate the installation.</span></span> <span data-ttu-id="11484-106">Este es un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="11484-106">This is a modal dialog box.</span></span>

<span data-ttu-id="11484-107">Este tipo de cuadro de diálogo normalmente contiene un [control de texto](text-control.md) y dos [botones](pushbutton-control.md)de control.</span><span class="sxs-lookup"><span data-stu-id="11484-107">This type of dialog box commonly contains a [Text control](text-control.md) and two [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="11484-108">Los dos botones proporcionan al usuario la opción de volver al último cuadro de diálogo o confirmar la finalización de la instalación.</span><span class="sxs-lookup"><span data-stu-id="11484-108">The two buttons give the user the choice of either returning to the last dialog box or confirming the termination of the installation.</span></span>

<span data-ttu-id="11484-109">[EndDialog](enddialog-controlevent.md) ControlEvent, está vinculado a estos dos botones en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="11484-109">The [EndDialog](enddialog-controlevent.md) ControlEvent is linked to these two buttons in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="11484-110">El parámetro *devuelto* de EndDialog ControlEvent, está vinculado a uno de los botones y hace que se termine el cuadro de diálogo **Cancelar** y que el foco vuelva al cuadro de diálogo anterior.</span><span class="sxs-lookup"><span data-stu-id="11484-110">The *Return* parameter of the EndDialog ControlEvent is linked to one of the buttons and causes the **Cancel** dialog box to be terminated and the focus to return to the previous dialog box.</span></span> <span data-ttu-id="11484-111">El parámetro *Exit* está vinculado al otro botón y hace que la interfaz de usuario devuelva el control al instalador con el código adecuado que indica que el usuario desea salir.</span><span class="sxs-lookup"><span data-stu-id="11484-111">The *Exit* parameter is linked to the other button and causes the user interface to return control to the installer with the appropriate code indicating that the user wants to exit.</span></span> <span data-ttu-id="11484-112">A continuación, el instalador se apaga y muestra el [cuadro de diálogo UserExit](userexit-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="11484-112">The installer then shuts down and displays the [UserExit Dialog](userexit-dialog.md).</span></span>

 

 



