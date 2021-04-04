---
title: Páginas de propiedades para su uso con especificadores de presentación
description: Active Directory Domain Services proporcionar un mecanismo para agregar páginas a la hoja de propiedades que se muestra para un objeto de directorio desde los complementos administrativos de Active Directory o el shell de Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- especificadores de presentación AD, páginas de propiedades para su uso con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904481"
---
# <a name="property-pages-for-use-with-display-specifiers"></a><span data-ttu-id="08cd9-104">Páginas de propiedades para su uso con especificadores de presentación</span><span class="sxs-lookup"><span data-stu-id="08cd9-104">Property Pages for Use with Display Specifiers</span></span>

<span data-ttu-id="08cd9-105">Active Directory Domain Services proporcionar un mecanismo para agregar páginas a la hoja de propiedades que se muestra para un objeto de directorio desde los complementos administrativos de Active Directory o el shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="08cd9-105">Active Directory Domain Services provide a mechanism for adding pages to the property sheet displayed for a directory object from the Active Directory administrative snap-ins or the Windows shell.</span></span> <span data-ttu-id="08cd9-106">Para agregar una página a la hoja de propiedades, implemente una extensión de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="08cd9-106">To add a page to the property sheet, implement a property sheet extension.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="08cd9-107">Audiencia de los desarrolladores</span><span class="sxs-lookup"><span data-stu-id="08cd9-107">Developer Audience</span></span>

<span data-ttu-id="08cd9-108">En esta documentación se supone que el lector está familiarizado con el funcionamiento COM y el desarrollo de componentes mediante C++.</span><span class="sxs-lookup"><span data-stu-id="08cd9-108">This documentation assumes that the reader is familiar with COM operation and component development using C++.</span></span> <span data-ttu-id="08cd9-109">En la actualidad, no es posible crear una extensión de hoja de propiedades Active Directory mediante Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="08cd9-109">It is not currently possible to create an Active Directory property sheet extension using Visual Basic.</span></span>

## <a name="creating-an-active-directory-property-sheet-extension"></a><span data-ttu-id="08cd9-110">Crear una Active Directory extensión de la hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="08cd9-110">Creating an Active Directory Property Sheet Extension</span></span>

<span data-ttu-id="08cd9-111">Una *extensión* de la hoja de propiedades es un servidor com en proceso que implementa ciertas interfaces y se registra con Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="08cd9-111">A *property sheet extension* is a COM in-proc server that implements certain interfaces and is registered with Active Directory Domain Services.</span></span> <span data-ttu-id="08cd9-112">Para crear una extensión de la hoja de propiedades, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="08cd9-112">To create a property sheet extension, perform the following steps.</span></span>

<span data-ttu-id="08cd9-113">**Para crear una Active Directory extensión de la hoja de propiedades**</span><span class="sxs-lookup"><span data-stu-id="08cd9-113">**To create an Active Directory property sheet extension**</span></span>

1.  <span data-ttu-id="08cd9-114">Cree el archivo DLL de extensión de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="08cd9-114">Create the property sheet extension DLL.</span></span> <span data-ttu-id="08cd9-115">Una extensión de la hoja de propiedades es un servidor COM en proceso que, como mínimo, implementa las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) y [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="08cd9-115">A property sheet extension is a COM in-proc server that, at a minimum, implements the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interfaces.</span></span> <span data-ttu-id="08cd9-116">Para obtener más información, vea [implementar el objeto com de la página de propiedades](implementing-the-property-page-com-object.md).</span><span class="sxs-lookup"><span data-stu-id="08cd9-116">For more information, see [Implementing the Property Page COM Object](implementing-the-property-page-com-object.md).</span></span>
2.  <span data-ttu-id="08cd9-117">Instale la extensión de la hoja de propiedades en los equipos donde se va a usar la extensión de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="08cd9-117">Install the property sheet extension on the computers where the property sheet extension is to be used.</span></span> <span data-ttu-id="08cd9-118">Para ello, cree un paquete de Microsoft Windows Installer para el archivo DLL de extensión de la hoja de propiedades e implemente el paquete adecuadamente mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="08cd9-118">To do this, create a Microsoft Windows Installer package for the property sheet extension DLL and deploy the package appropriately using the group policy.</span></span> <span data-ttu-id="08cd9-119">Para obtener más información, consulte [distribuir componentes](distributing-user-interface-components.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="08cd9-119">For more information, see [Distributing User Interface Components](distributing-user-interface-components.md).</span></span>
3.  <span data-ttu-id="08cd9-120">Registre la extensión de la hoja de propiedades en el registro de Windows y con Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="08cd9-120">Register the property sheet extension in the Windows registry and with Active Directory Domain Services.</span></span> <span data-ttu-id="08cd9-121">Para obtener más información, vea [registrar la página de propiedades de un objeto com en un especificador de presentación](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="08cd9-121">For more information, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>

 

 