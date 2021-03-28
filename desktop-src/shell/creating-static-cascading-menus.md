---
description: A partir de Windows 7, los menús en cascada se crean a través de la entrada del registro subcomandos, la entrada del registro ExtendedSubCommandsKey o la interfaz IExplorerCommand.
title: Crear menús en cascada estáticos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561443"
---
# <a name="creating-static-cascading-menus"></a><span data-ttu-id="42fa8-103">Crear menús en cascada estáticos</span><span class="sxs-lookup"><span data-stu-id="42fa8-103">Creating Static Cascading Menus</span></span>

<span data-ttu-id="42fa8-104">En Windows 7 y versiones posteriores, la implementación de menús en cascada se admite a través de la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="42fa8-104">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="42fa8-105">Antes de Windows 7, la creación de menús en cascada solo era posible a través de la implementación de la interfaz [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="42fa8-105">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="42fa8-106">En Windows 7 y versiones posteriores, debe recurrir a las soluciones basadas en código del modelo de objetos componentes (COM) solo cuando los métodos estáticos no sean suficientes.</span><span class="sxs-lookup"><span data-stu-id="42fa8-106">In Windows 7 and later, you should resort to Component Object Model (COM) code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="42fa8-107">La siguiente captura de pantalla proporciona un ejemplo de un menú en cascada.</span><span class="sxs-lookup"><span data-stu-id="42fa8-107">The following screen shot provides an example of a cascading menu.</span></span>

![captura de pantalla que muestra un ejemplo de un menú en cascada](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="42fa8-109">En Windows 7 y versiones posteriores, hay tres maneras de crear menús en cascada, que se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="42fa8-109">In Windows 7 and later, there are three ways to create cascading menus, which are described in the following sections.</span></span>

-   [<span data-ttu-id="42fa8-110">Cómo crear menús en cascada con la entrada del registro subcomandos</span><span class="sxs-lookup"><span data-stu-id="42fa8-110">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [<span data-ttu-id="42fa8-111">Cómo crear menús en cascada con la entrada del registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="42fa8-111">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [<span data-ttu-id="42fa8-112">Cómo crear menús en cascada con la interfaz IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="42fa8-112">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
