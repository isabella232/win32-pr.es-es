---
description: El uso de la funcionalidad de IMM en la aplicación compatible con IME libera a los usuarios de la necesidad de recordar todos los valores de caracteres posibles.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Acerca del administrador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687834"
---
# <a name="about-input-method-manager"></a><span data-ttu-id="77f45-103">Acerca del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="77f45-103">About Input Method Manager</span></span>

<span data-ttu-id="77f45-104">El uso de la funcionalidad de IMM en la aplicación compatible con IME libera a los usuarios de la necesidad de recordar todos los valores de caracteres posibles.</span><span class="sxs-lookup"><span data-stu-id="77f45-104">Use of the IMM functionality in your IME-aware application relieves users of the need to remember all possible character values.</span></span> <span data-ttu-id="77f45-105">En su lugar, permite que el IME supervise las pulsaciones de teclas de un usuario, prevea los caracteres que el usuario podría querer y presenta una lista de caracteres candidatos entre los que elegir.</span><span class="sxs-lookup"><span data-stu-id="77f45-105">Instead, it allows the IME to monitor a user's keystrokes, anticipates the characters the user might want, and presents a list of candidate characters from which to choose.</span></span>

> [!Note]  
> <span data-ttu-id="77f45-106">El IMM realiza operaciones similares a las del [marco de trabajo de servicios de texto](../tsf/text-services-framework.md), usadas por las aplicaciones que se comunican con los servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="77f45-106">The IMM performs similar operations to those of the [Text Services Framework](../tsf/text-services-framework.md), used by applications that communicate with text services.</span></span>

 

<span data-ttu-id="77f45-107">De forma predeterminada, el IMM proporciona una ventana IME a través de la cual el usuario introduce pulsaciones de teclas y vistas y selecciona candidatos.</span><span class="sxs-lookup"><span data-stu-id="77f45-107">By default, the IMM provides an IME window through which the user enters keystrokes and views and selects candidates.</span></span> <span data-ttu-id="77f45-108">Las aplicaciones pueden usar las funciones y los mensajes de IMM para crear y administrar sus propias ventanas de IME, proporcionando una interfaz personalizada mientras usa las capacidades de conversión del IME.</span><span class="sxs-lookup"><span data-stu-id="77f45-108">Applications can use the IMM functions and messages to create and manage their own IME windows, providing a custom interface while using the conversion capabilities of the IME.</span></span>

<span data-ttu-id="77f45-109">El IMM solo está habilitado en los sistemas operativos de Windows localizados de Asia Oriental (Chino, Japonés, Coreano).</span><span class="sxs-lookup"><span data-stu-id="77f45-109">The IMM is only enabled on East Asian (Chinese, Japanese, Korean) localized Windows operating systems.</span></span> <span data-ttu-id="77f45-110">En estos sistemas, la aplicación llama a [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ DBCSENABLED para determinar si el IMM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="77f45-110">On these systems, the application calls [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_DBCSENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="77f45-111">**Windows 2000:** La compatibilidad con el IMM completo se proporciona en todas las versiones de idioma localizadas.</span><span class="sxs-lookup"><span data-stu-id="77f45-111">**Windows 2000:** Full-featured IMM support is provided in all localized language versions.</span></span> <span data-ttu-id="77f45-112">Sin embargo, el IMM solo está habilitado cuando se instala un paquete de idioma asiático.</span><span class="sxs-lookup"><span data-stu-id="77f45-112">However, the IMM is enabled only when an Asian language pack is installed.</span></span> <span data-ttu-id="77f45-113">Una aplicación compatible con IME puede llamar a [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ IMMENABLED para determinar si el IMM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="77f45-113">An IME-aware application can call [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_IMMENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="77f45-114">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="77f45-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="77f45-115">Listas de candidatos</span><span class="sxs-lookup"><span data-stu-id="77f45-115">Candidate Lists</span></span>](candidate-lists.md)
-   [<span data-ttu-id="77f45-116">Cadena de composición</span><span class="sxs-lookup"><span data-stu-id="77f45-116">Composition String</span></span>](composition-string.md)
-   [<span data-ttu-id="77f45-117">HexToUnicode IME</span><span class="sxs-lookup"><span data-stu-id="77f45-117">HexToUnicode IME</span></span>](hextounicode-ime.md)
-   [<span data-ttu-id="77f45-118">Hot Keys</span><span class="sxs-lookup"><span data-stu-id="77f45-118">Hot Keys</span></span>](hot-keys.md)
-   [<span data-ttu-id="77f45-119">Mensajes IME</span><span class="sxs-lookup"><span data-stu-id="77f45-119">IME Messages</span></span>](ime-messages.md)
-   [<span data-ttu-id="77f45-120">Clase de ventana IME</span><span class="sxs-lookup"><span data-stu-id="77f45-120">IME Window Class</span></span>](ime-window-class.md)
-   [<span data-ttu-id="77f45-121">Contexto de entrada</span><span class="sxs-lookup"><span data-stu-id="77f45-121">Input Context</span></span>](input-context.md)
-   [<span data-ttu-id="77f45-122">Ventanas de estado, composición y candidatos</span><span class="sxs-lookup"><span data-stu-id="77f45-122">Status, Composition, and Candidates Windows</span></span>](status--composition--and-candidates-windows.md)

 

 
