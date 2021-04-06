---
description: Un componente es una parte de la aplicación o del producto que se va a instalar.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Componentes de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002245"
---
# <a name="windows-installer-components"></a><span data-ttu-id="f59ff-103">Componentes de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f59ff-103">Windows Installer Components</span></span>

<span data-ttu-id="f59ff-104">Un componente es una parte de la aplicación o del producto que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="f59ff-104">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="f59ff-105">Entre los ejemplos de componentes se incluyen archivos únicos, un grupo de archivos relacionados, objetos COM, registro, claves del registro, accesos directos, recursos, bibliotecas agrupadas en un directorio o fragmentos de código compartidos, como MFC o DAO.</span><span class="sxs-lookup"><span data-stu-id="f59ff-105">Examples of components include single files, a group of related files, COM objects, registration, registry keys, shortcuts, resources, libraries grouped into a directory, or shared pieces of code such as MFC or DAO.</span></span>

<span data-ttu-id="f59ff-106">El servicio del instalador instala o quita un componente como una única pieza coherente.</span><span class="sxs-lookup"><span data-stu-id="f59ff-106">The installer service installs or removes a component as a single coherent piece.</span></span> <span data-ttu-id="f59ff-107">Realiza un seguimiento de todos los componentes por el GUID del identificador de componente correspondiente especificado en la columna ComponentId de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f59ff-107">It tracks every component by the respective component ID GUID specified in the ComponentId column of the [Component table](component-table.md).</span></span>

> [!Note]  
> <span data-ttu-id="f59ff-108">Dos componentes que comparten el mismo identificador de componente se tratan como varias instancias del mismo componente, independientemente de su contenido real.</span><span class="sxs-lookup"><span data-stu-id="f59ff-108">Two components that share the same component ID are treated as multiple instances of the same component regardless of their actual content.</span></span> <span data-ttu-id="f59ff-109">Solo se instala una única instancia de cualquier componente en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f59ff-109">Only a single instance of any component is installed on a user's computer.</span></span> <span data-ttu-id="f59ff-110">Por lo tanto, varias características o aplicaciones pueden compartir algunos componentes.</span><span class="sxs-lookup"><span data-stu-id="f59ff-110">Several features or applications may therefore share some components.</span></span>

 

<span data-ttu-id="f59ff-111">Dado que los componentes suelen compartirse, el autor de un paquete de instalación debe seguir reglas estrictas al especificar los componentes de una característica o aplicación.</span><span class="sxs-lookup"><span data-stu-id="f59ff-111">Because components are commonly shared, the author of an installation package must follow strict rules when specifying the components of a feature or application.</span></span> <span data-ttu-id="f59ff-112">Esto es esencial para el funcionamiento correcto del mecanismo de recuento de referencias de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f59ff-112">This is essential for the correct operation of the Windows Installer reference-counting mechanism.</span></span> <span data-ttu-id="f59ff-113">Para obtener más información, vea [organizar aplicaciones en componentes](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="f59ff-113">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="f59ff-114">En Resumen, estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="f59ff-114">In brief, these rules are:</span></span>

-   <span data-ttu-id="f59ff-115">Cada componente debe almacenarse en una sola carpeta.</span><span class="sxs-lookup"><span data-stu-id="f59ff-115">Each component must be stored in a single folder.</span></span>
-   <span data-ttu-id="f59ff-116">Ningún archivo, entrada del registro, acceso directo u otros recursos deben enviarse como miembro de más de un componente.</span><span class="sxs-lookup"><span data-stu-id="f59ff-116">No file, registry entry, shortcut, or other resources should ever be shipped as a member of more than one component.</span></span> <span data-ttu-id="f59ff-117">Esto se aplica a los productos, versiones de producto y compañías.</span><span class="sxs-lookup"><span data-stu-id="f59ff-117">This applies across products, product versions, and companies.</span></span>

<span data-ttu-id="f59ff-118">Para obtener más información acerca del uso de los componentes de, vea.</span><span class="sxs-lookup"><span data-stu-id="f59ff-118">For more information about using components, see</span></span>

-   [<span data-ttu-id="f59ff-119">Instalación de un componente que falta</span><span class="sxs-lookup"><span data-stu-id="f59ff-119">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="f59ff-120">Instalación de componentes permanentes, archivos, fuentes y claves del registro</span><span class="sxs-lookup"><span data-stu-id="f59ff-120">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
-   [<span data-ttu-id="f59ff-121">Uso de componentes calificados</span><span class="sxs-lookup"><span data-stu-id="f59ff-121">Using Qualified Components</span></span>](using-qualified-components.md)
-   [<span data-ttu-id="f59ff-122">Uso de componentes transitivos</span><span class="sxs-lookup"><span data-stu-id="f59ff-122">Using Transitive Components</span></span>](using-transitive-components.md)
-   [<span data-ttu-id="f59ff-123">Trabajar con características y componentes</span><span class="sxs-lookup"><span data-stu-id="f59ff-123">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="f59ff-124">Crear un paquete grande</span><span class="sxs-lookup"><span data-stu-id="f59ff-124">Authoring a Large Package</span></span>](authoring-a-large-package.md)
-   [<span data-ttu-id="f59ff-125">Comprobar la instalación de características, componentes y archivos</span><span class="sxs-lookup"><span data-stu-id="f59ff-125">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
-   [<span data-ttu-id="f59ff-126">Buscar una característica o componente interrumpido</span><span class="sxs-lookup"><span data-stu-id="f59ff-126">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
-   [<span data-ttu-id="f59ff-127">Publicar productos, características y componentes</span><span class="sxs-lookup"><span data-stu-id="f59ff-127">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)

 

 



