---
description: La API del agente de Windows Update (WUA) es un conjunto de interfaces COM que permiten a los programadores y desarrolladores del sistema tener acceso a Windows Update y Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API del agente Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808648"
---
# <a name="windows-update-agent-api"></a><span data-ttu-id="231e9-103">API del agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="231e9-103">Windows Update Agent API</span></span>

## <a name="purpose"></a><span data-ttu-id="231e9-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="231e9-104">Purpose</span></span>

<span data-ttu-id="231e9-105">La API del agente de Windows Update (WUA) es un conjunto de interfaces COM que permiten a los programadores y desarrolladores del sistema tener acceso a Windows Update y [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="231e9-105">The Windows Update Agent (WUA) API is a set of COM interfaces that enable system administrators and programmers to access Windows Update and [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span></span> <span data-ttu-id="231e9-106">Se pueden escribir scripts y programas para examinar las actualizaciones que están disponibles actualmente para un equipo y, a continuación, puede instalar o desinstalar las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="231e9-106">Scripts and programs can be written to examine which updates are currently available for a computer, and then you can install or uninstall updates.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="231e9-107">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="231e9-107">Where applicable</span></span>

<span data-ttu-id="231e9-108">Los administradores del sistema pueden usar WUA para determinar mediante programación qué actualizaciones se deben aplicar a un equipo, descargar dichas actualizaciones y, a continuación, instalarlas con poca o ninguna intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="231e9-108">System administrators can use WUA to programmatically determine which updates should be applied to a computer, download those updates, and then install them with little or no user intervention.</span></span>

<span data-ttu-id="231e9-109">Los fabricantes de software independientes (ISV) y los desarrolladores de usuarios finales pueden integrar las características de WUA en el software de administración de equipos o de administración de actualizaciones para proporcionar un entorno operativo sin problemas.</span><span class="sxs-lookup"><span data-stu-id="231e9-109">Independent software vendors (ISV) and end-user developers can integrate WUA features into computer management or update management software to provide a seamless operating environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="231e9-110">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="231e9-110">Developer audience</span></span>

<span data-ttu-id="231e9-111">Puede escribir aplicaciones de WUA en varios lenguajes de programación.</span><span class="sxs-lookup"><span data-stu-id="231e9-111">You can write WUA applications in several programming languages.</span></span> <span data-ttu-id="231e9-112">WUA define interfaces y objetos a los que se puede tener acceso desde Visual Basic, Visual Basic Scripting Edition (VBScript), JScript y desde C y C++.</span><span class="sxs-lookup"><span data-stu-id="231e9-112">WUA defines interfaces and objects that are accessible from Visual Basic, Visual Basic Scripting Edition (VBScript), JScript, and from C and C++.</span></span> <span data-ttu-id="231e9-113">Una familiaridad con la programación COM es útil para el programador de WUA.</span><span class="sxs-lookup"><span data-stu-id="231e9-113">A familiarity with COM programming is useful to the WUA programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="231e9-114">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="231e9-114">Run-time requirements</span></span>

<span data-ttu-id="231e9-115">WUA se admite a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="231e9-115">WUA is supported starting with Windows XP.</span></span> <span data-ttu-id="231e9-116">WUA se admite en el servidor a partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="231e9-116">WUA is supported on the server starting with Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="231e9-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="231e9-117">In this section</span></span>

-   [<span data-ttu-id="231e9-118">Uso de la API del agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="231e9-118">Using the Windows Update Agent API</span></span>](using-the-windows-update-agent-api.md)
-   [<span data-ttu-id="231e9-119">Referencia de la API de WUA</span><span class="sxs-lookup"><span data-stu-id="231e9-119">WUA API Reference</span></span>](windows-update-agent--wua--api-reference.md)

 

 
