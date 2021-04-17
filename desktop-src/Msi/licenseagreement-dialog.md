---
description: Este cuadro de diálogo modal muestra el contrato de licencia para el usuario.
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: Cuadro de diálogo LicenseAgreement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686798"
---
# <a name="licenseagreement-dialog"></a><span data-ttu-id="90fab-103">Cuadro de diálogo LicenseAgreement</span><span class="sxs-lookup"><span data-stu-id="90fab-103">LicenseAgreement Dialog</span></span>

<span data-ttu-id="90fab-104">Este cuadro de diálogo modal muestra el contrato de licencia para el usuario.</span><span class="sxs-lookup"><span data-stu-id="90fab-104">This modal dialog box displays the license agreement to the user.</span></span> <span data-ttu-id="90fab-105">Normalmente, el cuadro de diálogo muestra el texto del acuerdo mediante un [control ScrollableText](scrollabletext-control.md) y un par de botones de opción que permiten al usuario aceptar o rechazar el contrato.</span><span class="sxs-lookup"><span data-stu-id="90fab-105">Typically the dialog box displays the text of the agreement using a [ScrollableText control](scrollabletext-control.md) and a pair of option buttons that let the user accept or reject the agreement.</span></span> <span data-ttu-id="90fab-106">Por motivos legales, es aconsejable que no se presente ningún botón al usuario como ya seleccionado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="90fab-106">For legal reasons it is advisable that neither button be presented to the user as already selected by default.</span></span> <span data-ttu-id="90fab-107">Esto obliga al usuario a establecer una opción activa.</span><span class="sxs-lookup"><span data-stu-id="90fab-107">This forces the user to make an active choice.</span></span> <span data-ttu-id="90fab-108">Normalmente, los autores usan un [control RadioButtonGroup](radiobuttongroup-control.md) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="90fab-108">Authors commonly use a [RadioButtonGroup control](radiobuttongroup-control.md) for this purpose.</span></span> <span data-ttu-id="90fab-109">Sin embargo, tenga en cuenta que el foco en un cuadro de diálogo no se mueve a un control RadioButtonGroup hasta que se ha seleccionado uno de los botones del grupo.</span><span class="sxs-lookup"><span data-stu-id="90fab-109">Note however that the focus on a dialog box does not move to a RadioButtonGroup control until one of the buttons in the group has been selected.</span></span>

 

 



