---
description: Usar menús dibujados por el propietario para admitir la funcionalidad de voz para Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Uso de menús de Owner-Drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809602"
---
# <a name="using-owner-drawn-menus"></a><span data-ttu-id="2c202-103">Uso de menús de Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="2c202-103">Using Owner-Drawn Menus</span></span>

<span data-ttu-id="2c202-104">Al usar menús dibujados por el propietario, debe hacer que los nombres de menú estén disponibles para admitir la funcionalidad de voz.</span><span class="sxs-lookup"><span data-stu-id="2c202-104">When using owner-drawn menus, you must make the menu names available to support speech functionality.</span></span> <span data-ttu-id="2c202-105">Existen dos formas de hacerlo:</span><span class="sxs-lookup"><span data-stu-id="2c202-105">There are two ways to do this:</span></span>

-   <span data-ttu-id="2c202-106">Exponga el nombre del elemento de menú mediante la estructura MSAAMENUINFO.</span><span class="sxs-lookup"><span data-stu-id="2c202-106">Expose the menu item name by using the MSAAMENUINFO structure.</span></span>
-   <span data-ttu-id="2c202-107">Proporcione una opción para reemplazar los menús gráficos por los menús de texto estándar cuando una ayuda de accesibilidad esté activa.</span><span class="sxs-lookup"><span data-stu-id="2c202-107">Provide an option to replace graphic menus with standard text menus when an accessibility aid is active.</span></span> <span data-ttu-id="2c202-108">Si la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) devuelve **true** con su parámetro *uiAction* establecido en SPI \_ GETSCREENREADER, use los menús estándar. La aplicación debe inspeccionar el mensaje de SETTINGSCHANGE de WM \_ y responder consultando el estado de esta opción y ajustando su presentación adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="2c202-108">If the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function returns **TRUE** with its *uiAction* parameter set to SPI\_GETSCREENREADER, use standard menus.The application should watch for the WM\_SETTINGSCHANGE message and respond by querying the state of this option and adjusting its display appropriately.</span></span> <span data-ttu-id="2c202-109">Por ejemplo, Microsoft Visual Studio proporciona una opción para usar los menús estándar en lugar de los menús personalizados que se muestran de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2c202-109">For example, Microsoft Visual Studio provides an option to use standard menus instead of the custom menus that are displayed by default.</span></span>

 

 
