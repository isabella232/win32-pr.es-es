---
description: A partir de Windows Vista, el TextInputPanel reemplaza a PenInputPanel para controlar el aspecto de la pantalla y el comportamiento del panel de entrada de Tablet PC. en las secciones siguientes se describe la programación del panel de entrada mediante las interfaces de programación de aplicaciones del panel de entrada de texto. TextInputPanel para los usuarios del panel de entrada de PenInputPanelUsing AutoCompleteEnabling corrección de texto para la entrada de lápiz personalizada CollectorsNote el panel de entrada de texto se implementa en un archivo ejecutable denominado TabTip.exe. La ejecución de TabTip.exe con el parámetro/SeekDesktop intenta ejecutar una versión reducida de la funcionalidad del panel de entrada en un escritorio interactivo no estándar, tal y como se crea con CreateDesktop. En el caso de la mayoría de los escritorios creados, el panel de entrada ya se ejecutará automáticamente en este modo. Este parámetro proporciona los medios para iniciarlo en escenarios de aplicaciones inusuales que, de otro modo, impiden el inicio automático. Si el panel de entrada ya se está ejecutando en el escritorio, este parámetro no tendrá ningún efecto y la instancia de TabTip.exe se cerrará inmediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programar el panel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720738"
---
# <a name="programming-the-text-input-panel"></a><span data-ttu-id="ef809-107">Programar el panel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="ef809-107">Programming the Text Input Panel</span></span>

<span data-ttu-id="ef809-108">A partir de Windows Vista, el [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) reemplaza a [**PenInputPanel**](peninputpanel-class.md) para controlar el aspecto de la pantalla y el comportamiento del panel de entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="ef809-108">Starting with Windows Vista, the [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) supersedes the [**PenInputPanel**](peninputpanel-class.md) for controlling the onscreen appearance and behavior of the Tablet Input Panel.</span></span>

<span data-ttu-id="ef809-109">En las secciones siguientes se describe la programación del panel de entrada mediante las interfaces de programación de aplicaciones del panel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="ef809-109">The following sections describe programming the Input Panel using the Text Input Panel application programming interfaces.</span></span>

-   [<span data-ttu-id="ef809-110">TextInputPanel para los usuarios de PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="ef809-110">TextInputPanel for Users of PenInputPanel</span></span>](textinputpanel-for-users-of-peninputpanel.md)
-   [<span data-ttu-id="ef809-111">Uso de autocompletar del panel de entrada</span><span class="sxs-lookup"><span data-stu-id="ef809-111">Using Input Panel AutoComplete</span></span>](using-input-panel-autocomplete.md)
-   [<span data-ttu-id="ef809-112">Habilitar la corrección de texto para los recopiladores de tinta personalizados</span><span class="sxs-lookup"><span data-stu-id="ef809-112">Enabling Text Correction for Custom Ink Collectors</span></span>](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> <span data-ttu-id="ef809-113">El panel de entrada de texto se implementa en un archivo ejecutable denominado TabTip.exe.</span><span class="sxs-lookup"><span data-stu-id="ef809-113">The Text Input Panel is implemented in an executable file called TabTip.exe.</span></span> <span data-ttu-id="ef809-114">La ejecución de TabTip.exe con el parámetro */SeekDesktop* intenta ejecutar una versión reducida de la funcionalidad del panel de entrada en un escritorio interactivo no estándar, tal y como se crea con [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="ef809-114">Running TabTip.exe with the */SeekDesktop* parameter attempts to run a reduced functionality version of Input Panel on a nonstandard interactive desktop, as created with [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span> <span data-ttu-id="ef809-115">En el caso de la mayoría de los escritorios creados, el panel de entrada ya se ejecutará automáticamente en este modo.</span><span class="sxs-lookup"><span data-stu-id="ef809-115">For most created desktops, Input Panel will automatically run in this mode already.</span></span> <span data-ttu-id="ef809-116">Este parámetro proporciona los medios para iniciarlo en escenarios de aplicaciones inusuales que, de otro modo, impiden el inicio automático.</span><span class="sxs-lookup"><span data-stu-id="ef809-116">This parameter provides the means for launching it in unusual application scenarios that otherwise prevent the automatic launch.</span></span> <span data-ttu-id="ef809-117">Si el panel de entrada ya se está ejecutando en el escritorio, este parámetro no tendrá ningún efecto y la instancia de TabTip.exe se cerrará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ef809-117">If Input Panel is already running on the desktop, this parameter will have no effect and the instance of TabTip.exe will exit immediately.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ef809-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef809-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef809-119">Programar el panel de entrada mediante la clase PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="ef809-119">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
