---
title: Alta resolución de PPP para aplicaciones de escritorio en Windows 8.1
description: Alta resolución de PPP para aplicaciones de escritorio en Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704981"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a><span data-ttu-id="fd569-103">Alta resolución de PPP para aplicaciones de escritorio en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fd569-103">High DPI for desktop apps in Windows 8.1</span></span>

## <a name="platforms"></a><span data-ttu-id="fd569-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="fd569-104">Platforms</span></span>

<dl> <span data-ttu-id="fd569-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fd569-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="fd569-106">Servidores: Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fd569-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="fd569-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd569-107">Description</span></span>

<span data-ttu-id="fd569-108">En Windows 8.1 se espera que las aplicaciones de escritorio se ejecuten en pantallas con un ajuste de escala del 200%, además de los 100%, 125% y el escalado de 150% que se admite en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd569-108">In Windows 8.1 desktop applications are expected to run on displays with 200% scaling in addition to the 100%, 125%, and 150% scaling that is supported in Windows 8.</span></span> <span data-ttu-id="fd569-109">Además, las aplicaciones de escritorio se escalan por monitor en lugar de a un único factor de escala aplicado a todas las pantallas.</span><span class="sxs-lookup"><span data-stu-id="fd569-109">In addition, desktop applications are scaled on a per-monitor basis rather than to a single scale factor applied to all displays.</span></span> <span data-ttu-id="fd569-110">Los desarrolladores también pueden llamar a nuevas API en Windows 8.1 para obtener los factores de escala de cada monitor.</span><span class="sxs-lookup"><span data-stu-id="fd569-110">Developers can also call new APIs in Windows 8.1 to get per-monitor scale factors.</span></span>

## <a name="manifestations"></a><span data-ttu-id="fd569-111">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="fd569-111">Manifestations</span></span>

<span data-ttu-id="fd569-112">Los usuarios pueden usar nuevas pantallas de alta densidad con Windows 8.1 para disfrutar de una experiencia visual increíble que aprovecha los datos de píxeles más altos.</span><span class="sxs-lookup"><span data-stu-id="fd569-112">Users can use new high density displays with Windows 8.1 for a terrific visual experience that takes advantage of the higher pixel data.</span></span> <span data-ttu-id="fd569-113">Si las aplicaciones no controlan los PPP altos, Windows las escalará para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fd569-113">If applications don’t handle high DPI, Windows will scale them for the user.</span></span> <span data-ttu-id="fd569-114">Además, los usuarios pueden usar una combinación de pantallas de densidad alta y baja en el mismo equipo, y Windows escalará el contenido de forma adecuada para cada pantalla.</span><span class="sxs-lookup"><span data-stu-id="fd569-114">In addition, users can use a mix of high and low density displays on the same computer, and Windows will scale content appropriately for each display.</span></span> <span data-ttu-id="fd569-115">Se trata de una mejora respecto a Windows 8, donde el contenido puede ser demasiado grande en algunas pantallas.</span><span class="sxs-lookup"><span data-stu-id="fd569-115">This is an improvement over Windows 8, where content can be too large on some displays.</span></span>

## <a name="mitigation"></a><span data-ttu-id="fd569-116">Mitigación</span><span class="sxs-lookup"><span data-stu-id="fd569-116">Mitigation</span></span>

<span data-ttu-id="fd569-117">Puesto que Windows escalará las aplicaciones que no se escalan por sí mismas, los desarrolladores no suelen tener que realizar trabajo adicional, pero los desarrolladores que invierten en la escritura de aplicaciones que admiten un alto nivel de PPP tendrán una ventaja competitiva, ya que esas aplicaciones tendrán un aspecto mejor en los nuevos portátiles y monitores de escritorio altos de PPP.</span><span class="sxs-lookup"><span data-stu-id="fd569-117">Since Windows will scale apps that don’t scale themselves, developers generally do not have to do additional work, but developers who do invest in writing applications that support high DPI will have a competitive advantage, as those applications will look better on new high DPI laptops and desktop monitors.</span></span>

## <a name="solution"></a><span data-ttu-id="fd569-118">Solución</span><span class="sxs-lookup"><span data-stu-id="fd569-118">Solution</span></span>

<span data-ttu-id="fd569-119">La realización de una aplicación que puede aprovechar las ventajas de los PPP altos es una tarea compleja de diseño e implementación.</span><span class="sxs-lookup"><span data-stu-id="fd569-119">Making an application that can take advantage of high DPI is a complex design and implementation task.</span></span> <span data-ttu-id="fd569-120">Vea los vínculos siguientes para obtener información del tutorial, compilar contenido de presentación y compatibilidad similar.</span><span class="sxs-lookup"><span data-stu-id="fd569-120">See the links below for tutorial information, BUILD presentation content, and similar support.</span></span>

## <a name="tests"></a><span data-ttu-id="fd569-121">Pruebas</span><span class="sxs-lookup"><span data-stu-id="fd569-121">Tests</span></span>

<span data-ttu-id="fd569-122">Aunque los desarrolladores no decidan que sus aplicaciones aprovechen las ventajas de un alto nivel de PPP, deben probar su aplicación en 100%, 125%, 150% y el escalado de 200% para asegurarse de que la experiencia del usuario final es satisfactoria y competitiva.</span><span class="sxs-lookup"><span data-stu-id="fd569-122">Even if developers do not choose to make their applications take advantage of high DPI, they should test their application at 100%, 125%, 150%, and 200% scaling to be sure the end-user experience is satisfactory and competitive.</span></span>

## <a name="resources"></a><span data-ttu-id="fd569-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="fd569-123">Resources</span></span>

-   [<span data-ttu-id="fd569-124">Notas del producto y tutorial sobre la alta resolución de PPP en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fd569-124">White paper and tutorial on high DPI in Windows 8.1</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [<span data-ttu-id="fd569-125">Programas de ejemplo de escritorio de Windows</span><span class="sxs-lookup"><span data-stu-id="fd569-125">Windows desktop sample programs</span></span>](https://www.microsoft.com/?ref=go)
-   [<span data-ttu-id="fd569-126">Sesión de división de compilación 2013 en alta resolución de PPP en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fd569-126">BUILD 2013 break-out session on high DPI in Windows 8.1</span></span>](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 