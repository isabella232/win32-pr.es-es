---
description: En esta sección se describen las funciones de devolución de llamada del shell de Windows.
title: Funciones de devolución de llamada de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423719"
---
# <a name="shell-callback-functions"></a><span data-ttu-id="ebe15-103">Funciones de devolución de llamada de Shell</span><span class="sxs-lookup"><span data-stu-id="ebe15-103">Shell Callback Functions</span></span>

<span data-ttu-id="ebe15-104">En esta sección se describen las funciones de devolución de llamada del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="ebe15-104">This section describes the Windows Shell callback functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ebe15-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ebe15-105">In this section</span></span>



| <span data-ttu-id="ebe15-106">Tema</span><span class="sxs-lookup"><span data-stu-id="ebe15-106">Topic</span></span>                                                                     | <span data-ttu-id="ebe15-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebe15-107">Description</span></span>                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe15-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ebe15-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span></span><br/>                      | <span data-ttu-id="ebe15-109">Especifica una función de devolución de llamada definida por la aplicación que se usa para enviar y procesar mensajes desde un cuadro de diálogo de **exploración** mostrado en respuesta a una llamada a [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="ebe15-109">Specifies an application-defined callback function used to send messages to, and process messages from, a **Browse** dialog box displayed in response to a call to [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span><br/> |
| [<span data-ttu-id="ebe15-110">*FMExtensionProc*</span><span class="sxs-lookup"><span data-stu-id="ebe15-110">*FMExtensionProc*</span></span>](fmextensionproc.md)<br/>                       | <span data-ttu-id="ebe15-111">Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos para comunicarse con una extensión del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="ebe15-111">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span><br/>                                                                                            |
| [<span data-ttu-id="ebe15-112">*MRUCMPPROC*</span><span class="sxs-lookup"><span data-stu-id="ebe15-112">*MRUCMPPROC*</span></span>](mrucmpproc.md)<br/>                                 | <span data-ttu-id="ebe15-113">Se usa para determinar si un elemento está presente en una lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="ebe15-113">Used to determine whether an item is present in a most recently used (MRU) list.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="ebe15-114">**PAPPSTATE \_ , \_ rutina de cambio**</span><span class="sxs-lookup"><span data-stu-id="ebe15-114">**PAPPSTATE\_CHANGE\_ROUTINE**</span></span>](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | <span data-ttu-id="ebe15-115">Especifica una función de devolución de llamada definida por la aplicación que notifica a la aplicación cuando la aplicación entra o sale de un estado suspendido.</span><span class="sxs-lookup"><span data-stu-id="ebe15-115">Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.</span></span><br/>                                                                                            |
| [<span data-ttu-id="ebe15-116">**SUBCLASSPROC**</span><span class="sxs-lookup"><span data-stu-id="ebe15-116">**SUBCLASSPROC**</span></span>](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | <span data-ttu-id="ebe15-117">Define el prototipo de la función de devolución de llamada usada por [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) y [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span><span class="sxs-lookup"><span data-stu-id="ebe15-117">Defines the prototype for the callback function used by [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) and [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span></span><br/>                                                   |
| [<span data-ttu-id="ebe15-118">**\_proc UNdelete de FM \_**</span><span class="sxs-lookup"><span data-stu-id="ebe15-118">**FM\_UNDELETE\_PROC**</span></span>](undeletefile.md)<br/>                     | <span data-ttu-id="ebe15-119">Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos cuando el usuario elige el comando **Undelete** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="ebe15-119">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span><br/>                                                                   |



 

 

 
