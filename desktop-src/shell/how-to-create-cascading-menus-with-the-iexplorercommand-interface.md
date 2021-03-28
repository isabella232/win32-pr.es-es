---
description: 'Otra opción para agregar verbos a un menú en cascada es a través de IExplorerCommand:: EnumSubCommands.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Crear menús en cascada con la interfaz IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104563422"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="2b3c3-103">Cómo crear menús en cascada con la interfaz IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="2b3c3-103">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="2b3c3-104">Otra opción para agregar verbos a un menú en cascada es a través de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="2b3c3-104">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="2b3c3-105">Este método habilita los orígenes de datos que proporcionan los comandos del módulo de comandos a través de la interfaz [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esos comandos como verbos en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-105">This method enables data sources that provide their command module commands through the [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) interface to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="2b3c3-106">En Windows 7 y versiones posteriores, puede proporcionar la misma implementación de verbo mediante la interfaz [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) que puede con la interfaz [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="2b3c3-106">In Windows 7 and later, you can provide the same verb implementation using the [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) interface as you can with the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span>

## <a name="instructions"></a><span data-ttu-id="2b3c3-107">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="2b3c3-107">Instructions</span></span>


<span data-ttu-id="2b3c3-108">En las dos capturas de pantalla siguientes se muestra el uso de menús en cascada en la carpeta **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="2b3c3-108">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos.](images/file-assoc/filecascademenu.png)

![captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a><span data-ttu-id="2b3c3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b3c3-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2b3c3-112">Dado que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) solo admite la activación en proceso, se recomienda para su uso por parte de los orígenes de datos de Shell que necesitan compartir la implementación entre los comandos y los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="2b3c3-112">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2b3c3-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b3c3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b3c3-114">**IExplorerCommand**</span><span class="sxs-lookup"><span data-stu-id="2b3c3-114">**IExplorerCommand**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[<span data-ttu-id="2b3c3-115">**IExplorerCommandProvider**</span><span class="sxs-lookup"><span data-stu-id="2b3c3-115">**IExplorerCommandProvider**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[<span data-ttu-id="2b3c3-116">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="2b3c3-116">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
