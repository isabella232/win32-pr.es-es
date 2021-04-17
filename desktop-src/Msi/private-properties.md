---
description: El instalador usa internamente las propiedades privadas y los valores deben ser especificados en la base de datos por el autor del paquete de instalación o por el instalador durante la instalación en los valores determinados por el entorno operativo.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Propiedades privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652887"
---
# <a name="private-properties"></a><span data-ttu-id="def98-103">Propiedades privadas</span><span class="sxs-lookup"><span data-stu-id="def98-103">Private Properties</span></span>

<span data-ttu-id="def98-104">El instalador usa internamente las propiedades privadas y los valores deben ser especificados en la base de datos por el autor del paquete de instalación o por el instalador durante la instalación en los valores determinados por el entorno operativo.</span><span class="sxs-lookup"><span data-stu-id="def98-104">Private properties are used internally by the installer and their values must be entered into the database by the author of the installation package or set by the installer during the installation to values determined by the operating environment.</span></span> <span data-ttu-id="def98-105">La única forma en que un usuario puede interactuar con las propiedades privadas es a través de los [eventos de control](control-events.md) en la interfaz de usuario creada del paquete.</span><span class="sxs-lookup"><span data-stu-id="def98-105">The only way a user can interact with private properties is through [Control Events](control-events.md) in the package's authored user interface.</span></span> <span data-ttu-id="def98-106">Los nombres de propiedad privados deben incluir minúsculas.</span><span class="sxs-lookup"><span data-stu-id="def98-106">Private property names must include lowercase letters.</span></span> <span data-ttu-id="def98-107">Vea [restricciones en los nombres de propiedad](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="def98-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="def98-108">Las propiedades privadas normalmente describen el entorno operativo.</span><span class="sxs-lookup"><span data-stu-id="def98-108">Private properties commonly describe the operating environment.</span></span> <span data-ttu-id="def98-109">Por ejemplo, si la instalación se ejecuta en una plataforma Windows, el instalador establece la propiedad [**WindowsFolder**](windowsfolder.md) en el valor especificado en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="def98-109">For example, if the installation is run on a Windows platform, the installer sets the [**WindowsFolder**](windowsfolder.md) property to the value specified in the Property table.</span></span>

<span data-ttu-id="def98-110">Los valores de propiedad privados no se pueden invalidar en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="def98-110">Private property values cannot be overridden at a command line.</span></span> <span data-ttu-id="def98-111">Para borrar una propiedad privada de una instalación, déjela fuera de la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="def98-111">To clear a private property from an installation, leave it out of the [Property table](property-table.md).</span></span> <span data-ttu-id="def98-112">En Windows XP y Windows 2000 no se puede establecer una propiedad privada en la fase de la interfaz de usuario de la instalación y, a continuación, pasar el valor a la fase de ejecución.</span><span class="sxs-lookup"><span data-stu-id="def98-112">On Windows XP, and Windows 2000 you cannot set a private property in the user interface phase of the installation and then pass the value to the execution phase.</span></span>

<span data-ttu-id="def98-113">Para obtener una lista de todas las propiedades privadas estándar que usa el instalador, consulte [referencia de propiedades](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="def98-113">For a list of all the standard private properties used by the installer, see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="def98-114">Puede definir una propiedad privada personalizada especificando el nombre y el valor inicial de la propiedad en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="def98-114">You can define a custom private property by entering the property's name and initial value in the Property table.</span></span> <span data-ttu-id="def98-115">Los nombres de propiedad privados siempre deben incluir minúsculas.</span><span class="sxs-lookup"><span data-stu-id="def98-115">Private property names must always include lowercase letters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="def98-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="def98-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="def98-117">Propiedades públicas</span><span class="sxs-lookup"><span data-stu-id="def98-117">Public Properties</span></span>](public-properties.md)
</dt> </dl>

 

 



