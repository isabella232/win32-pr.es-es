---
title: Cadena de enlace
description: Debido al número de objetos a los que se puede tener acceso desde un servicio de directorio, pueden producirse conflictos de nomenclatura.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- ADSI de cadena de enlace
- ADsPath ADSI, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995620"
---
# <a name="binding-string"></a><span data-ttu-id="edfa8-105">Cadena de enlace</span><span class="sxs-lookup"><span data-stu-id="edfa8-105">Binding String</span></span>

<span data-ttu-id="edfa8-106">Debido al número de objetos a los que se puede tener acceso desde un servicio de directorio, pueden producirse conflictos de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="edfa8-106">Due to the number of objects accessible from a directory service, naming collisions can occur.</span></span> <span data-ttu-id="edfa8-107">La cadena de enlace, que se conoce comúnmente como ADsPath, le permite especificar un objeto determinado sin producir una colisión de nombres.</span><span class="sxs-lookup"><span data-stu-id="edfa8-107">The binding string, which is commonly referred to as the ADsPath, enables you to specify a particular object without causing a naming collision.</span></span> <span data-ttu-id="edfa8-108">Esto se puede aplicar a un único proveedor de servicios de directorio o a través de varios proveedores de servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="edfa8-108">This can be applied for a single directory service provider or across multiple directory service providers.</span></span>

<span data-ttu-id="edfa8-109">ADsPath es una cadena que identifica de forma única un objeto ADSI en un servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="edfa8-109">An ADsPath is a string that uniquely identifies an ADSI object on a directory service.</span></span> <span data-ttu-id="edfa8-110">Dado que los objetos ADSI existen en el contexto del espacio de nombres del servicio de directorio subyacente, parte de la sintaxis de un nombre ADsPath es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="edfa8-110">Because ADSI objects exist within the context of the namespace of the underlying directory service, part of the syntax of an ADsPath name is provider-specific.</span></span>

<span data-ttu-id="edfa8-111">En la tabla siguiente se enumeran los proveedores ADSI proporcionados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="edfa8-111">The following table lists the ADSI providers provided by default.</span></span>



| <span data-ttu-id="edfa8-112">Proveedor</span><span class="sxs-lookup"><span data-stu-id="edfa8-112">Provider</span></span>         | <span data-ttu-id="edfa8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="edfa8-113">Description</span></span>                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edfa8-114">WinNT</span><span class="sxs-lookup"><span data-stu-id="edfa8-114">WinNT</span></span><br/> | <span data-ttu-id="edfa8-115">Se usa para comunicarse con los controladores de dominio de Windows.</span><span class="sxs-lookup"><span data-stu-id="edfa8-115">Used to communicate with Windows domain controllers.</span></span> <span data-ttu-id="edfa8-116">Para obtener más información sobre el ADsPath de WinNT, consulte [WinNT ADsPath](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="edfa8-116">For more information about the WinNT ADsPath, see [WinNT ADsPath](winnt-adspath.md).</span></span><br/>           |
| <span data-ttu-id="edfa8-117">LDAP</span><span class="sxs-lookup"><span data-stu-id="edfa8-117">LDAP</span></span><br/>  | <span data-ttu-id="edfa8-118">Se utiliza para comunicarse con servidores LDAP, como Active Directory.</span><span class="sxs-lookup"><span data-stu-id="edfa8-118">Used to communicate with LDAP servers, such as Active Directory.</span></span> <span data-ttu-id="edfa8-119">Para obtener más información acerca de la ADsPath de LDAP, consulte [ADsPath de LDAP](ldap-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="edfa8-119">For more information about the LDAP ADsPath, see [LDAP ADsPath](ldap-adspath.md).</span></span><br/>  |
| <span data-ttu-id="edfa8-120">Anuncios</span><span class="sxs-lookup"><span data-stu-id="edfa8-120">ADs</span></span><br/>   | <span data-ttu-id="edfa8-121">Proporciona una implementación de [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) que se puede utilizar para enumerar todos los proveedores ADSI instalados en el cliente.</span><span class="sxs-lookup"><span data-stu-id="edfa8-121">Provides an [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) implementation that can be used to enumerate all of the ADSI providers installed on the client.</span></span><br/> |



 

<span data-ttu-id="edfa8-122">Use estos nombres de proveedor para tener acceso al espacio de nombres del proveedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="edfa8-122">Use these provider names to access the default provider namespace.</span></span> <span data-ttu-id="edfa8-123">Por ejemplo, si se enlaza a LDAP, ADSI se enlaza a un contenedor que contiene el objeto de dominio que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="edfa8-123">For example, if you bind to LDAP, ADSI binds to a container that contains the domain object currently logged on.</span></span> <span data-ttu-id="edfa8-124">Si se enlaza a WinNT, ADSI enlaza a un contenedor que contiene objetos que se correlacionan con todos los dominios de la red.</span><span class="sxs-lookup"><span data-stu-id="edfa8-124">If you bind to WinNT, ADSI binds to a container that holds objects that correlate to all domains on the network.</span></span>

<span data-ttu-id="edfa8-125">Los elementos iniciales de la cadena ADsPath son el identificador de programación (progID) del proveedor ADSI, seguido de "://", seguido de la sintaxis dictada por el espacio de nombres del proveedor.</span><span class="sxs-lookup"><span data-stu-id="edfa8-125">The initial elements of the ADsPath string are the programmatic identifier (progID) of the ADSI provider, followed by "://", followed by syntax dictated by the provider namespace.</span></span> <span data-ttu-id="edfa8-126">La cadena progID puede o no distinguir mayúsculas de minúsculas, dependiendo del proveedor.</span><span class="sxs-lookup"><span data-stu-id="edfa8-126">The progID string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="edfa8-127">Las cadenas progID para los proveedores enumerados anteriormente distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="edfa8-127">The progID strings for the providers listed above are case-sensitive.</span></span>

<span data-ttu-id="edfa8-128">La cadena de ruta de acceso puede distinguir entre mayúsculas y minúsculas, en función del proveedor.</span><span class="sxs-lookup"><span data-stu-id="edfa8-128">The path string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="edfa8-129">Las cadenas de ruta de acceso de los proveedores enumerados anteriormente no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="edfa8-129">The path strings for the providers listed above are not case-sensitive.</span></span>

<span data-ttu-id="edfa8-130">A continuación se muestran ejemplos de ADsPaths.</span><span class="sxs-lookup"><span data-stu-id="edfa8-130">The following are examples of ADsPaths.</span></span>

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

<span data-ttu-id="edfa8-131">Para buscar todos los proveedores instalados en el equipo, enlace al proveedor de ADs tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="edfa8-131">To find all providers installed on your computer, bind to the ADs provider as shown in the following code example.</span></span>


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



<span data-ttu-id="edfa8-132">Con el proveedor LDAP, puede especificar el ADsPath en un formulario de nombre distintivo X. 500 (DN), empezando por la etiqueta CN, o puede especificar su inversa jerárquica, empezando por la etiqueta O.</span><span class="sxs-lookup"><span data-stu-id="edfa8-132">Using the LDAP provider, you can specify the ADsPath either in an X.500 distinguished name (DN) form, starting with the CN tag, or you can specify its hierarchical inverse, starting with the O tag.</span></span> <span data-ttu-id="edfa8-133">El formato que se usa en el ADsPath inicial determina el orden de las etiquetas.</span><span class="sxs-lookup"><span data-stu-id="edfa8-133">The form you use in the initial ADsPath determines the order of the tags.</span></span>

<span data-ttu-id="edfa8-134">En la tabla siguiente se enumeran los caracteres especiales de ADsPath.</span><span class="sxs-lookup"><span data-stu-id="edfa8-134">The following table lists ADsPath special characters.</span></span>



| <span data-ttu-id="edfa8-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="edfa8-135">Name</span></span>                      | <span data-ttu-id="edfa8-136">Carácter</span><span class="sxs-lookup"><span data-stu-id="edfa8-136">Character</span></span>           | <span data-ttu-id="edfa8-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="edfa8-137">Description</span></span>                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edfa8-138">Comilla doble</span><span class="sxs-lookup"><span data-stu-id="edfa8-138">Double quote</span></span><br/>   | <span data-ttu-id="edfa8-139">"</span><span class="sxs-lookup"><span data-stu-id="edfa8-139">"</span></span><br/>        | <span data-ttu-id="edfa8-140">Se usa para citar cualquier parte del ADsPath que pueda contener un carácter especial para que la cadena se interprete literalmente.</span><span class="sxs-lookup"><span data-stu-id="edfa8-140">Used to quote any part of the ADsPath that may contain a special character so that the string is interpreted literally.</span></span> <span data-ttu-id="edfa8-141">Por ejemplo, "CN = nombre/prefijo".</span><span class="sxs-lookup"><span data-stu-id="edfa8-141">For example, "CN=Name/Prefix".</span></span><br/>                                     |
| <span data-ttu-id="edfa8-142">Barra diagonal inversa</span><span class="sxs-lookup"><span data-stu-id="edfa8-142">Backslash</span></span><br/>      | \\<br/>       | <span data-ttu-id="edfa8-143">Se usa para anteponer caracteres especiales para indicar que deben usarse como literales.</span><span class="sxs-lookup"><span data-stu-id="edfa8-143">Used to precede special characters to signify they should be used as literals.</span></span> <span data-ttu-id="edfa8-144">Para obtener más información y una lista de caracteres especiales, consulte [nombres distintivos](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="edfa8-144">For more information and a list of special characters, see [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span><br/> |
| <span data-ttu-id="edfa8-145">Slash</span><span class="sxs-lookup"><span data-stu-id="edfa8-145">Slash</span></span><br/>          | /<br/>        | <span data-ttu-id="edfa8-146">Separador de componentes.</span><span class="sxs-lookup"><span data-stu-id="edfa8-146">Component separator.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="edfa8-147">Corchetes angulares</span><span class="sxs-lookup"><span data-stu-id="edfa8-147">Angle brackets</span></span><br/> | <><br/> | <span data-ttu-id="edfa8-148">Delimite un ADsPath dentro de otra Convención de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="edfa8-148">Delimit an ADsPath within another naming convention.</span></span><br/>                                                                                                                                       |



 

<span data-ttu-id="edfa8-149">Para delimitar una ADsPath en una especificación de búsqueda o como parte de una dirección URL, use el corchete angular de apertura y derecha (< >).</span><span class="sxs-lookup"><span data-stu-id="edfa8-149">To delimit an ADsPath in a search specification or as part of a URL, use the left and right angle bracket (< >).</span></span> <span data-ttu-id="edfa8-150">Por ejemplo, " &lt; WinNT://mydomain/UserAccount &gt; ".</span><span class="sxs-lookup"><span data-stu-id="edfa8-150">For example, "&lt;WinNT://MyDomain/UserAccount&gt;".</span></span>

<span data-ttu-id="edfa8-151">Algunos proveedores ADSI pueden haber agregado restricciones de sintaxis debido a los requisitos de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="edfa8-151">Some ADSI providers may have added syntax restrictions due to namespace requirements.</span></span>

## <a name="active-directory-binding-options"></a><span data-ttu-id="edfa8-152">Opciones de enlace de Active Directory</span><span class="sxs-lookup"><span data-stu-id="edfa8-152">Active Directory Binding Options</span></span>

<span data-ttu-id="edfa8-153">Active Directory proporciona la capacidad de enlazar a un objeto utilizando varios otros tipos de cadenas de enlace, como un identificador único global (GUID) COM o un identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="edfa8-153">Active Directory provides the ability to bind to an object using several other types of binding strings, such as a COM globally unique identifier (GUID) or a security identifier (SID).</span></span> <span data-ttu-id="edfa8-154">Para obtener más información, vea [enlazar a Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="edfa8-154">For more information, see [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span></span>

 

