---
description: Una forma de crear aplicaciones web habilitadas para la entrada de lápiz consiste en colocar Windows Forms controles dentro de awebpagewithin Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Controles Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705541"
---
# <a name="web-controls"></a><span data-ttu-id="1bab5-103">Controles Web</span><span class="sxs-lookup"><span data-stu-id="1bab5-103">Web Controls</span></span>

<span data-ttu-id="1bab5-104">Una forma de crear aplicaciones web habilitadas para la entrada de lápiz consiste en colocar Windows Forms controles dentro de awebpagewithin Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1bab5-104">One way to create ink-enabled Web applications is to put Windows Forms controls inside awebpagewithin Microsoft Internet Explorer.</span></span> <span data-ttu-id="1bab5-105">Puede encontrar un buen tutorial sobre esta técnica en [uso de Windows Forms controles en Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span><span class="sxs-lookup"><span data-stu-id="1bab5-105">A good tutorial on this technique can be found at [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx).</span></span> <span data-ttu-id="1bab5-106">Los pasos básicos del tutorial son:</span><span class="sxs-lookup"><span data-stu-id="1bab5-106">The basic steps in the tutorial are:</span></span>

1.  <span data-ttu-id="1bab5-107">Cree un control que herede de [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="1bab5-107">Create a control that inherits from [**System.Windows.Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).</span></span>
2.  <span data-ttu-id="1bab5-108">Cree una página HTML con una etiqueta de objeto que haga referencia a ese UserControl.</span><span class="sxs-lookup"><span data-stu-id="1bab5-108">Create an HTML page with an object tag that refers to that UserControl.</span></span>
3.  <span data-ttu-id="1bab5-109">Cree un directorio virtual y establezca permisos.</span><span class="sxs-lookup"><span data-stu-id="1bab5-109">Create a virtual directory and set permissions.</span></span>
4.  <span data-ttu-id="1bab5-110">Cargue la dirección URL de la página HTML en el explorador.</span><span class="sxs-lookup"><span data-stu-id="1bab5-110">Load the URL of the HTML page into the browser.</span></span>

<span data-ttu-id="1bab5-111">Esta técnica se puede aplicar a los controles habilitados para tinta, al igual que cualquier otro [**control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)de Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="1bab5-111">This technique can be applied to ink-enabled controls, just like any other Windows Forms [**Control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="1bab5-112">De hecho, la técnica se puede usar con cualquier clase en el marco de Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="1bab5-112">In fact, the technique can be used with any class in the Microsoft .NET Framework.</span></span> <span data-ttu-id="1bab5-113">Los ejemplos proporcionados por el kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition incluyen una versión de control Web del ejemplo de notificaciones automáticas en la sección ejemplos de la Web de tinta.</span><span class="sxs-lookup"><span data-stu-id="1bab5-113">The samples provided by the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) include a Web control version of the Auto Claims sample in the Ink Web Samples section.</span></span> <span data-ttu-id="1bab5-114">En este ejemplo se toma el [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md) original y se convierte en un control que se coloca en una página web.</span><span class="sxs-lookup"><span data-stu-id="1bab5-114">This example takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span> <span data-ttu-id="1bab5-115">Para obtener más información sobre la habilitación de este ejemplo en Web, vea el [ejemplo de control de entrada Web de lápiz](ink-web-control-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1bab5-115">For more information about Web-enabling this sample, see the [Ink Web Control Sample](ink-web-control-sample.md).</span></span>

> [!Note]  
> <span data-ttu-id="1bab5-116">Cuando se implementa una aplicación creada con .NET a través de la web, la aplicación puede verse afectada por el modelo de seguridad de .NET.</span><span class="sxs-lookup"><span data-stu-id="1bab5-116">When you deploy an application created by using .NET over the Web, the application may be affected by security model for .NET.</span></span> <span data-ttu-id="1bab5-117">Para obtener más información sobre cómo funciona la seguridad con las aplicaciones web habilitadas para tinta, consulte [seguridad y confianza](security-and-trust.md).</span><span class="sxs-lookup"><span data-stu-id="1bab5-117">For more information about how security works with ink-enabled Web applications, see [Security and Trust](security-and-trust.md).</span></span>

 

 

 
