---
description: Windows Installer implementa un número de controles estándar que los autores de paquetes pueden colocar en los cuadros de diálogo. Sin embargo, no todos los controles estándar de Microsoft Windows están disponibles y no se pueden crear controles personalizados para usarlos con la interfaz de usuario del instalador.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Información general sobre los controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669751"
---
# <a name="controls-overview"></a><span data-ttu-id="cf972-104">Información general sobre los controles</span><span class="sxs-lookup"><span data-stu-id="cf972-104">Controls Overview</span></span>

<span data-ttu-id="cf972-105">Windows Installer implementa un número de controles estándar que los autores de paquetes pueden colocar en los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cf972-105">Windows Installer implements a number of standard controls that package authors can place onto dialog boxes.</span></span> <span data-ttu-id="cf972-106">Sin embargo, no todos los controles estándar de Microsoft Windows están disponibles y no se pueden crear controles personalizados para usarlos con la interfaz de usuario del instalador.</span><span class="sxs-lookup"><span data-stu-id="cf972-106">However, not all standard Microsoft Windows controls are available, and custom controls cannot be created for use with the installer UI.</span></span>

<span data-ttu-id="cf972-107">Los controles se crean en los cuadros de diálogo del instalador de manera similar a cómo se crean los cuadros de diálogo mediante programación con la API de la interfaz de usuario de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cf972-107">Controls are created on dialog boxes in the installer in a manner similar to how dialog boxes are created programmatically using the Microsoft Windows user interface API.</span></span> <span data-ttu-id="cf972-108">Se crea un control a partir de una plantilla registrada en la tabla de control.</span><span class="sxs-lookup"><span data-stu-id="cf972-108">A control is created from a template recorded in the Control table.</span></span> <span data-ttu-id="cf972-109">Esta plantilla es ligeramente diferente en que contiene el nombre único del cuadro de diálogo en el que aparece el control.</span><span class="sxs-lookup"><span data-stu-id="cf972-109">This template is slightly different in that it contains the unique name of the dialog box on which the control appears.</span></span>

<span data-ttu-id="cf972-110">En la API de la interfaz de usuario de Microsoft Windows, la interacción con el usuario se logra mediante la creación de una función de devolución de llamada para controlar los mensajes enviados por el control.</span><span class="sxs-lookup"><span data-stu-id="cf972-110">In the Microsoft Windows user interface API, user interaction is accomplished by creating a callback function to handle messages posted by the control.</span></span> <span data-ttu-id="cf972-111">Además, la mayoría de los controles de Microsoft Windows reciben mensajes, como los enviados por la función [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="cf972-111">Also, most Microsoft Windows controls receive messages, such as those sent by the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="cf972-112">La comunicación entre el usuario y los controles se realiza en el instalador mediante el uso de [ControlEvents](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cf972-112">Communication between the user and controls is accomplished in the installer through the use of [ControlEvents](controlevent-overview.md).</span></span> <span data-ttu-id="cf972-113">Sin embargo, hay un conjunto limitado de ControlEvents que son específicos de cada control en el conjunto limitado de controles de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cf972-113">However, there is a limited set of ControlEvents that are specific to each control in the limited set of controls in Windows Installer.</span></span> <span data-ttu-id="cf972-114">Los controles pueden publicar más de un ControlEvent, y pueden recibir más de un ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="cf972-114">Controls may post more than one ControlEvent and may receive more than one ControlEvent.</span></span>

<span data-ttu-id="cf972-115">Los controles pueden publicar ControlEvents específicos mediante el uso de la tabla ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="cf972-115">Controls can publish specific ControlEvents through the use of the ControlEvent table.</span></span> <span data-ttu-id="cf972-116">Los controles pueden recibir ControlEvents mediante el uso de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="cf972-116">Controls can receive ControlEvents through the use of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="cf972-117">Windows Installer publica ControlEvents durante la ejecución de algunas acciones también y los controles suscritos a estos ControlEvents en la tabla EventMapping los reciben.</span><span class="sxs-lookup"><span data-stu-id="cf972-117">Windows Installer publishes ControlEvents during the execution of some actions as well, and controls subscribed to these ControlEvents in the EventMapping table receive them.</span></span>

 

 
