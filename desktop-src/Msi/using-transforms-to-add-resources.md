---
description: Los recursos necesarios para la personalización de una aplicación, como las plantillas corporativas, se pueden implementar con la aplicación mediante la inclusión de una transformación con el paquete de instalación de la aplicación.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Usar transformaciones para agregar recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677908"
---
# <a name="using-transforms-to-add-resources"></a><span data-ttu-id="2436f-103">Usar transformaciones para agregar recursos</span><span class="sxs-lookup"><span data-stu-id="2436f-103">Using Transforms to Add Resources</span></span>

<span data-ttu-id="2436f-104">Los recursos necesarios para la personalización de una aplicación, como las plantillas corporativas, se pueden implementar con la aplicación mediante la inclusión de una transformación con el paquete de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2436f-104">Resources that are needed for the customization of an application, such as corporate templates, can be deployed with the application by including a transform with the application's installation package.</span></span> <span data-ttu-id="2436f-105">Se deben seguir las reglas siguientes al implementar recursos, como archivos, claves del registro o accesos directos, mediante una transformación.</span><span class="sxs-lookup"><span data-stu-id="2436f-105">The following rules should be followed when deploying resources, such as files, registry keys, or shortcuts, using a transform.</span></span>

-   <span data-ttu-id="2436f-106">La transformación debe agregar uno o varios componentes nuevos a la base de datos de instalación para que contenga los recursos adicionales.</span><span class="sxs-lookup"><span data-stu-id="2436f-106">The transform should add one or more new components to the installation database to contain the additional resources.</span></span> <span data-ttu-id="2436f-107">La transformación no debe agregar recursos a un componente que ya existe en la instalación de.</span><span class="sxs-lookup"><span data-stu-id="2436f-107">The transform should not add resources to a component that already exists in the installation.</span></span>
-   <span data-ttu-id="2436f-108">La transformación debe agregar una o varias características nuevas a la base de datos de instalación para que contenga estos componentes nuevos.</span><span class="sxs-lookup"><span data-stu-id="2436f-108">The transform should add one or more new features to the installation database to contain these new components.</span></span> <span data-ttu-id="2436f-109">Estas nuevas características no deben ser los elementos primarios de las características existentes, pero las nuevas características principales y secundarias se pueden introducir juntas.</span><span class="sxs-lookup"><span data-stu-id="2436f-109">These new features should not be the parents of any existing features, but new parent and child features may be introduced together.</span></span> <span data-ttu-id="2436f-110">Las nuevas características deben tener nombres que sean únicos en todas las demás transformaciones de este producto.</span><span class="sxs-lookup"><span data-stu-id="2436f-110">New features should be given names that are unique across all other transforms for this product.</span></span> <span data-ttu-id="2436f-111">Dos transformaciones no deberían agregar una característica a este producto que tenga el mismo nombre que aparece en la columna característica de la [tabla de características](feature-table.md) y que contiene componentes o recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="2436f-111">No two transforms should ever add a feature to this product that has the same name listed in the Feature column of the [Feature table](feature-table.md) and containing different components or resources.</span></span>

 

 



