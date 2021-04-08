---
title: Registrar la extensión de creación de objetos
description: Cuando se crea un archivo DLL de extensión de creación de objetos en Active Directory Domain Services, se debe registrar con el registro de Windows y Active Directory Domain Services para que COM y los complementos de MMC administrativos de Active Directory conozcan la extensión.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995064"
---
# <a name="registering-the-object-creation-extension"></a><span data-ttu-id="b6a35-103">Registrar la extensión de creación de objetos</span><span class="sxs-lookup"><span data-stu-id="b6a35-103">Registering the Object Creation Extension</span></span>

<span data-ttu-id="b6a35-104">Cuando se crea un archivo DLL de extensión de creación de objetos en Active Directory Domain Services, se debe registrar con el registro de Windows y Active Directory Domain Services para que COM y los complementos de MMC administrativos de Active Directory conozcan la extensión.</span><span class="sxs-lookup"><span data-stu-id="b6a35-104">When an object creation extension DLL in Active Directory Domain Services is created, it must be registered with the Windows registry and Active Directory Domain Services to make COM and the Active Directory administrative MMC snap-ins aware of the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="b6a35-105">Registro en el registro de Windows</span><span class="sxs-lookup"><span data-stu-id="b6a35-105">Registering in the Windows Registry</span></span>

<span data-ttu-id="b6a35-106">Al igual que todos los servidores COM, una extensión de creación de objetos debe estar registrada en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6a35-106">Like all COM servers, an object creation extension must be registered in the Windows registry.</span></span> <span data-ttu-id="b6a35-107">La extensión se registra con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="b6a35-107">The extension is registered under the following key:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

<span data-ttu-id="b6a35-108">" &lt; extensión CLSID &gt; " es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="b6a35-108">"&lt;extension CLSID&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="b6a35-109">" &lt; ruta de acceso de la extensión &gt; " contiene la ruta de acceso y el nombre del archivo dll de extensión.</span><span class="sxs-lookup"><span data-stu-id="b6a35-109">"&lt;extension path&gt;" contains the path and file name of the extension DLL.</span></span> <span data-ttu-id="b6a35-110">El valor **ThreadingModel** para todas las extensiones de creación de objetos debe ser "Apartamento".</span><span class="sxs-lookup"><span data-stu-id="b6a35-110">The **ThreadingModel** value for all object creation extensions must be "Apartment".</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="b6a35-111">Registro con Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="b6a35-111">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="b6a35-112">El registro de la extensión de creación de objetos es específico de una configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b6a35-112">Object creation extension registration is specific to one locale.</span></span> <span data-ttu-id="b6a35-113">Si la extensión de creación de objetos se aplica a todas las configuraciones regionales, debe registrarse en el objeto **displaySpecifier** de la clase de objeto en todos los subcontenedores de la configuración regional del contenedor DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="b6a35-113">If the object creation extension applies to all locales, it must be registered in the object class's **displaySpecifier** object in all of the locale subcontainers in the DisplaySpecifiers container.</span></span> <span data-ttu-id="b6a35-114">Si la extensión de creación de objetos está localizada para una configuración regional determinada, regístrela en el objeto **displaySpecifier** en el subcontenedor de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b6a35-114">If the object creation extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale's subcontainer.</span></span> <span data-ttu-id="b6a35-115">Para obtener más información sobre el contenedor DisplaySpecifiers y las configuraciones regionales, consulte [especificadores de pantalla](display-specifiers.md) y [contenedor de DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="b6a35-115">For more information about the DisplaySpecifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="b6a35-116">Hay dos atributos DisplaySpecifier en los que se puede registrar una extensión de creación de objetos.</span><span class="sxs-lookup"><span data-stu-id="b6a35-116">There are two DisplaySpecifier attributes that an object creation extension can be registered under.</span></span> <span data-ttu-id="b6a35-117">Son **creationWizard** y **createWizardExt**.</span><span class="sxs-lookup"><span data-stu-id="b6a35-117">These are **creationWizard** and **createWizardExt**.</span></span>

<span data-ttu-id="b6a35-118">El atributo **creationWizard** identifica las extensiones de creación de objetos principales para reemplazar el Asistente para creación de objetos existente o nativo en Active Directory complementos administrativos. Una extensión de creación principal proporciona el primer conjunto de páginas y se hospeda de la misma manera que las páginas nativas.</span><span class="sxs-lookup"><span data-stu-id="b6a35-118">The **creationWizard** attribute identifies primary object creation extensions to replace the existing or native object creation wizard in Active Directory administrative snap-ins. A primary creation extension provides the first set of pages and is hosted in the same way as native pages.</span></span> <span data-ttu-id="b6a35-119">Este atributo tiene un único valor y requiere el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="b6a35-119">This attribute is single-valued and requires the following format:</span></span>


```C++
<CLSID>
```



<span data-ttu-id="b6a35-120">El " &lt; CLSID &gt; " es la representación de cadena del CLSID del objeto com tal y como lo ha producido la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="b6a35-120">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="b6a35-121">El atributo **createWizardExt** identifica las extensiones de creación de objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b6a35-121">The **createWizardExt** attribute identifies secondary object creation extensions.</span></span> <span data-ttu-id="b6a35-122">Una extensión de creación secundaria agrega páginas del asistente a las páginas nativas o a la extensión principal.</span><span class="sxs-lookup"><span data-stu-id="b6a35-122">A secondary creation extension adds wizard pages to the native pages or primary extension.</span></span> <span data-ttu-id="b6a35-123">Este atributo tiene varios valores y requiere el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="b6a35-123">This attribute is multi-valued and requires the following format:</span></span>


```C++
<order number>,<CLSID>
```



<span data-ttu-id="b6a35-124">El " &lt; número de pedido &gt; " es un número sin signo que representa la posición de la página en el asistente.</span><span class="sxs-lookup"><span data-stu-id="b6a35-124">The "&lt;order number&gt;" is an unsigned number that represents the page's position in the wizard.</span></span> <span data-ttu-id="b6a35-125">Cuando se muestra un asistente para creación, los valores se ordenan mediante una comparación de "número de &lt; pedido" de cada valor &gt; .</span><span class="sxs-lookup"><span data-stu-id="b6a35-125">When a creation wizard is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="b6a35-126">Si hay más de un valor con el mismo " &lt; número de pedido &gt; ", esas páginas se cargan en el orden en que se leen en el servidor de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b6a35-126">If more than one value has the same "&lt;order number&gt;", those pages are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="b6a35-127">Si es posible, debe usar un " &lt; número de pedido" no existente &gt; (es decir, uno que no haya usado otros valores de la propiedad).</span><span class="sxs-lookup"><span data-stu-id="b6a35-127">If possible, you should use a non-existing "&lt;order number&gt;" (that is, one that has not been used by other values in the property).</span></span> <span data-ttu-id="b6a35-128">No hay ninguna posición de inicio prescrita y se permiten huecos en la &lt; secuencia "número de pedido &gt; ".</span><span class="sxs-lookup"><span data-stu-id="b6a35-128">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="b6a35-129">El " &lt; CLSID &gt; " es la representación de cadena del CLSID del objeto com tal y como lo ha producido la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="b6a35-129">The "&lt;CLSID&gt;" is the string representation of the COM object's CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

 

 