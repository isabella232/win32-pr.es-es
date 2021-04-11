---
description: Windows Installer puede configurar la instalación de software mediante los valores de las variables definidas en un paquete de instalación o por el usuario.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Acerca de las propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276540"
---
# <a name="about-properties"></a><span data-ttu-id="7cff2-103">Acerca de las propiedades</span><span class="sxs-lookup"><span data-stu-id="7cff2-103">About Properties</span></span>

<span data-ttu-id="7cff2-104">Windows Installer puede configurar la instalación de software mediante los valores de las variables definidas en un paquete de instalación o por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7cff2-104">Windows Installer can configure software installation by using the values of variables defined in an installation package or by the user.</span></span>

<span data-ttu-id="7cff2-105">Windows Installer usa tres categorías de variables globales durante una instalación:</span><span class="sxs-lookup"><span data-stu-id="7cff2-105">Windows Installer uses three categories of global variables during an installation:</span></span>

-   <span data-ttu-id="7cff2-106">Propiedades privadas: el instalador usa propiedades privadas internamente y sus valores se deben crear en la base de datos de instalación o establecerse en los valores determinados por el entorno operativo.</span><span class="sxs-lookup"><span data-stu-id="7cff2-106">Private properties: The installer uses private properties internally and their values must be authored into the installation database or set to values determined by the operating environment.</span></span>
-   <span data-ttu-id="7cff2-107">Propiedades públicas: las propiedades públicas se pueden crear en la base de datos y cambiar por un administrador de usuarios o del sistema en la línea de comandos, mediante la aplicación de una transformación o mediante la interacción con una interfaz de usuario creada.</span><span class="sxs-lookup"><span data-stu-id="7cff2-107">Public properties: Public properties can be authored into the database and changed by a user or system administrator on the command line, by applying a transform, or by interacting with an authored user interface.</span></span>
-   <span data-ttu-id="7cff2-108">Propiedades públicas restringidas: por motivos de seguridad, el autor de un paquete de instalación puede restringir las propiedades públicas que un usuario puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="7cff2-108">Restricted public properties: For security purposes, the author of an installation package can restrict the public properties a user can change.</span></span>

<span data-ttu-id="7cff2-109">No todas las propiedades deben definirse en cada paquete, hay un pequeño conjunto de propiedades necesarias que se deben definir en cada paquete.</span><span class="sxs-lookup"><span data-stu-id="7cff2-109">Not all properties need to be defined in every package, there is a small set of required properties that must be defined in every package.</span></span> <span data-ttu-id="7cff2-110">El instalador establece los valores de las propiedades en un orden de prioridad determinado.</span><span class="sxs-lookup"><span data-stu-id="7cff2-110">The installer sets the values of properties in a particular order of precedence.</span></span>

[<span data-ttu-id="7cff2-111">Propiedades privadas</span><span class="sxs-lookup"><span data-stu-id="7cff2-111">Private Properties</span></span>](private-properties.md)

[<span data-ttu-id="7cff2-112">Propiedades públicas</span><span class="sxs-lookup"><span data-stu-id="7cff2-112">Public Properties</span></span>](public-properties.md)

[<span data-ttu-id="7cff2-113">Propiedades públicas restringidas</span><span class="sxs-lookup"><span data-stu-id="7cff2-113">Restricted Public Properties</span></span>](restricted-public-properties.md)

[<span data-ttu-id="7cff2-114">Propiedades obligatorias</span><span class="sxs-lookup"><span data-stu-id="7cff2-114">Required Properties</span></span>](required-properties.md)

[<span data-ttu-id="7cff2-115">Orden de prioridad de propiedad</span><span class="sxs-lookup"><span data-stu-id="7cff2-115">Order of Property Precedence</span></span>](order-of-property-precedence.md)

## <a name="related-topics"></a><span data-ttu-id="7cff2-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7cff2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cff2-117">Utilizar propiedades</span><span class="sxs-lookup"><span data-stu-id="7cff2-117">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="7cff2-118">Referencia de propiedades</span><span class="sxs-lookup"><span data-stu-id="7cff2-118">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



