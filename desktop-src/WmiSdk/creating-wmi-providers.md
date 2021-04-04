---
description: Los desarrolladores pueden ampliar la infraestructura de WMI mediante el desarrollo de proveedores de WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Crear proveedores de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083463"
---
# <a name="creating-wmi-providers"></a><span data-ttu-id="dd2c4-103">Crear proveedores de WMI</span><span class="sxs-lookup"><span data-stu-id="dd2c4-103">Creating WMI Providers</span></span>

<span data-ttu-id="dd2c4-104">Los desarrolladores pueden ampliar la infraestructura de WMI mediante el desarrollo de proveedores de WMI.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-104">Developers can extend the WMI infrastructure by developing WMI providers.</span></span> <span data-ttu-id="dd2c4-105">Los proveedores WMI son objetos COM que implementan un conjunto especificado de interfaces y, hasta el momento, se implementan siempre en C++.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-105">WMI providers are COM objects that implement a specified set of interfaces and, until recently, were always implemented in C++.</span></span> <span data-ttu-id="dd2c4-106">Ahora puede usar lenguajes administrados como C# para implementar proveedores de WMI.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-106">You can now use managed languages like C# to implement WMI providers.</span></span> <span data-ttu-id="dd2c4-107">La versión 3,5 de .NET Framework presentó el marco de trabajo de extensiones de proveedor WMI que lo hace posible.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-107">Version 3.5 of the .NET framework introduced the WMI Provider Extensions framework that makes this possible.</span></span> <span data-ttu-id="dd2c4-108">Para obtener más información sobre la creación de proveedores de WMI con ese marco de trabajo, lea el artículo sobre la [escritura de proveedores de WMI acoplados mediante la extensión de proveedor de WMI.NET 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="dd2c4-108">To learn more about creating WMI providers by using that framework, read the article, [Writing coupled WMI providers using WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="dd2c4-109">También puede crear un proveedor mediante la infraestructura de administración de Windows (MI), la versión de la próxima generación de WMI.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-109">You can also create a provider using Windows Management Infrastructure (MI), the next-generation version of WMI.</span></span> <span data-ttu-id="dd2c4-110">Para obtener más información, vea [cómo implementar un proveedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="dd2c4-110">For more information, see [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span></span>

 

<span data-ttu-id="dd2c4-111">En la tabla siguiente se describe el contenido de esta sección.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-111">The following table describes the contents in this section.</span></span>



| <span data-ttu-id="dd2c4-112">Tema</span><span class="sxs-lookup"><span data-stu-id="dd2c4-112">Topic</span></span>                                                      | <span data-ttu-id="dd2c4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd2c4-113">Description</span></span>                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="dd2c4-114">Proporcionar datos a WMI</span><span class="sxs-lookup"><span data-stu-id="dd2c4-114">Providing Data to WMI</span></span>](providing-data-to-wmi.md)         | <span data-ttu-id="dd2c4-115">Proporciona información general sobre los pasos necesarios para crear un proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-115">Provides an overview of the steps involved in creating a WMI provider.</span></span>         |
| [<span data-ttu-id="dd2c4-116">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="dd2c4-116">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md) | <span data-ttu-id="dd2c4-117">Describe las tareas que debe realizar al crear varios tipos de proveedores de WMI.</span><span class="sxs-lookup"><span data-stu-id="dd2c4-117">Describes tasks you must perform when creating various types of WMI providers.</span></span> |



 

 

 
