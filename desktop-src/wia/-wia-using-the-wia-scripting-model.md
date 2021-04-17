---
description: A través del modelo de scripting de WIA, la funcionalidad de adquisición de imágenes de Windows (WIA) se pone a disposición de los lenguajes de scripting, como el software de desarrollo de Microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y los lenguajes de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.
ms.assetid: eec5dc91-7b32-4f38-bdfe-c11bddc17ba2
title: Usar el modelo de scripting de WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: affa2c4368a83b2d67c1c6219b76040ba043a1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696505"
---
# <a name="using-the-wia-scripting-model"></a><span data-ttu-id="30a2e-103">Usar el modelo de scripting de WIA</span><span class="sxs-lookup"><span data-stu-id="30a2e-103">Using the WIA Scripting Model</span></span>

<span data-ttu-id="30a2e-104">A través del [modelo de scripting de WIA](-wia-wia-scripting-model.md), la funcionalidad de adquisición de imágenes de Windows (WIA) se pone a disposición de los lenguajes de scripting, como el software de desarrollo de Microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y los lenguajes de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="30a2e-104">Through the [WIA Scripting Model](-wia-wia-scripting-model.md), Windows Image Acquisition (WIA) functionality is made available to scripting languages such as Microsoft JScript development software and Microsoft Visual Basic Scripting Edition (VBScript), and high-level languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="30a2e-105">Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="30a2e-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="30a2e-106">Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="30a2e-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="30a2e-107">El modelo de scripting de WIA expone objetos que heredan la interfaz [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="30a2e-107">The WIA scripting model exposes objects that inherit the [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

<span data-ttu-id="30a2e-108">El modelo de scripting ofrece una versión simplificada de WIAAPI.</span><span class="sxs-lookup"><span data-stu-id="30a2e-108">The scripting model offers a simplified version of the WIAAPI.</span></span>

<span data-ttu-id="30a2e-109">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="30a2e-109">For more information, see the following:</span></span>

-   [<span data-ttu-id="30a2e-110">Configurar el entorno de desarrollo del modelo de scripting</span><span class="sxs-lookup"><span data-stu-id="30a2e-110">Setting up the Scripting Model Development Environment</span></span>](-wia-setting-up-the-scripting-model.md)
-   [<span data-ttu-id="30a2e-111">Conexión a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="30a2e-111">Connecting to a Device</span></span>](-wia-connecting-to-a-device.md)
-   [<span data-ttu-id="30a2e-112">Navegar por un árbol de objetos de elemento</span><span class="sxs-lookup"><span data-stu-id="30a2e-112">Navigating a Tree of Item Objects</span></span>](-wia-navigating-a-tree-of-item-objects.md)
-   [<span data-ttu-id="30a2e-113">Transferir datos</span><span class="sxs-lookup"><span data-stu-id="30a2e-113">Transferring Data</span></span>](-wia-transferring-data.md)
-   [<span data-ttu-id="30a2e-114">Limitaciones del modelo de scripting</span><span class="sxs-lookup"><span data-stu-id="30a2e-114">Limitations of the Scripting Model</span></span>](-wia-limitations-of-the-scripting-model.md)

 

 
