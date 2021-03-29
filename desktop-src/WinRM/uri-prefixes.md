---
title: Prefijos de URI
description: El prefijo del URI del recurso es diferente en función del esquema XML que describe el recurso.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103904888"
---
# <a name="uri-prefixes"></a><span data-ttu-id="bd4f9-103">Prefijos de URI</span><span class="sxs-lookup"><span data-stu-id="bd4f9-103">URI prefixes</span></span>

<span data-ttu-id="bd4f9-104">El prefijo del [*URI del recurso*](windows-remote-management-glossary.md) es diferente en función del esquema XML que describe el recurso.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-104">The [*resource URI*](windows-remote-management-glossary.md) prefix is different depending on which XML schema describes the resource.</span></span>

## <a name="prefixes"></a><span data-ttu-id="bd4f9-105">Prefijos</span><span class="sxs-lookup"><span data-stu-id="bd4f9-105">Prefixes</span></span>

<span data-ttu-id="bd4f9-106">Si obtiene acceso a una clase [*cim*](windows-remote-management-glossary.md) 2,1, como [**el \_ archivo de archivos CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), el prefijo del URI difiere del prefijo de una clase CIM 2,9, **como \_ AdminDomain de CIM**.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-106">If you access a [*CIM*](windows-remote-management-glossary.md) 2.1 class, such as [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), the prefix of the URI differs from the prefix for a CIM 2.9 class, such as **CIM\_AdminDomain**.</span></span> <span data-ttu-id="bd4f9-107">Las clases CIM 2,1 se documentan en la sección [clases CIM](/windows/desktop/WmiSdk/cimclas) de instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bd4f9-107">CIM 2.1 classes are documented in the [CIM Classes](/windows/desktop/WmiSdk/cimclas) section of Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="bd4f9-108">La mayoría de [las clases de WMI](/windows/desktop/WmiSdk/wmi-classes) se encuentran en el espacio de nombres WMI de **\\ cimv2 raíz** .</span><span class="sxs-lookup"><span data-stu-id="bd4f9-108">Most [WMI classes](/windows/desktop/WmiSdk/wmi-classes) are in the **root\\cimv2** WMI namespace.</span></span> <span data-ttu-id="bd4f9-109">Las clases del proveedor de la interfaz de administración de plataforma inteligente ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) de Microsoft se encuentran en el **\\ hardware raíz**.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-109">Classes for the Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) provider are in **root\\hardware**.</span></span>

<span data-ttu-id="bd4f9-110">La lista siguiente contiene los prefijos de URI de recurso para estos esquemas:</span><span class="sxs-lookup"><span data-stu-id="bd4f9-110">The following list contains the resource URI prefixes for these schemas:</span></span>

-   <span data-ttu-id="bd4f9-111">Clases WMI o CIM 2,1 en el espacio de nombres **root \\ cimv2**</span><span class="sxs-lookup"><span data-stu-id="bd4f9-111">WMI or CIM 2.1 classes in the **root\\cimv2** namespace</span></span>

    <span data-ttu-id="bd4f9-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span><span class="sxs-lookup"><span data-stu-id="bd4f9-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span></span>

-   <span data-ttu-id="bd4f9-113">Clases CIM 2,9 o clases IPMI</span><span class="sxs-lookup"><span data-stu-id="bd4f9-113">CIM 2.9 classes or IPMI classes</span></span>

    <span data-ttu-id="bd4f9-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span><span class="sxs-lookup"><span data-stu-id="bd4f9-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span></span>

-   <span data-ttu-id="bd4f9-115">Manera alternativa de obtener acceso a las clases del proveedor de IPMI</span><span class="sxs-lookup"><span data-stu-id="bd4f9-115">Alternate way to access IPMI provider classes</span></span>

    <span data-ttu-id="bd4f9-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span><span class="sxs-lookup"><span data-stu-id="bd4f9-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span></span>

<span data-ttu-id="bd4f9-117">Para obtener más información, vea [URI de recursos](resource-uris.md) y cadenas de [UrlPrefix](/windows/desktop/Http/urlprefix-strings).</span><span class="sxs-lookup"><span data-stu-id="bd4f9-117">For more information, see [Resource URIs](resource-uris.md) and [UrlPrefix Strings](/windows/desktop/Http/urlprefix-strings).</span></span> <span data-ttu-id="bd4f9-118">Para obtener más información sobre cómo generar un URI para un método o una clase WMI, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="bd4f9-118">For more information about generating a URI for a WMI class or method, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="prefix-aliases"></a><span data-ttu-id="bd4f9-119">Alias de prefijo</span><span class="sxs-lookup"><span data-stu-id="bd4f9-119">Prefix Aliases</span></span>

<span data-ttu-id="bd4f9-120">Un alias de prefijo es un acceso directo que representa el prefijo de URI de recurso largo.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-120">A prefix alias is a shortcut that represents the long resource URI prefix.</span></span> <span data-ttu-id="bd4f9-121">También puede utilizar alias en la línea de comandos de **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="bd4f9-121">You can also use aliases in the **Winrm** command-line.</span></span> <span data-ttu-id="bd4f9-122">Para ver una lista de los alias disponibles, escriba **alias de ayuda de WinRM**.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-122">To view a list of available aliases, type **Winrm help aliases**.</span></span>

<span data-ttu-id="bd4f9-123">Tenga en cuenta que no se puede usar un alias dentro de una referencia de punto de conexión (EPR) al especificar un URI de recurso.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-123">Be aware that an alias cannot be used inside an endpoint reference (EPR) when specifying a resource URI.</span></span> <span data-ttu-id="bd4f9-124">Administración remota de Windows no puede expandir el alias cuando está incrustado en XML.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-124">Windows Remote Management is unable to expand the alias when it is embedded in XML.</span></span>

<span data-ttu-id="bd4f9-125">En el ejemplo de código siguiente, el alias de WinRM se usa en un EPR en lugar de en el URI de recurso completo, que es `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` .</span><span class="sxs-lookup"><span data-stu-id="bd4f9-125">In the following code example, the winrm alias is used in an EPR instead of the complete resource URI, which is `http://schemas.microsoft.com/wbem/wsman/1/config/Listener`.</span></span> <span data-ttu-id="bd4f9-126">En este caso, WinRM devuelve un error que indica que el servicio no puede procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-126">In this case, WinRM returns an error that indicates the service cannot process the request.</span></span>


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



<span data-ttu-id="bd4f9-127">A continuación se enumeran los alias definidos y los URI de recursos para los que se sustituyen.</span><span class="sxs-lookup"><span data-stu-id="bd4f9-127">The following lists defined aliases and resource URIs for which they substitute.</span></span>

<dl> <dt>

<span data-ttu-id="bd4f9-128"><span id="wmi"></span><span id="WMI"></span>WMI</span><span class="sxs-lookup"><span data-stu-id="bd4f9-128"><span id="wmi"></span><span id="WMI"></span>wmi</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span data-ttu-id="bd4f9-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span><span class="sxs-lookup"><span data-stu-id="bd4f9-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span data-ttu-id="bd4f9-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span><span class="sxs-lookup"><span data-stu-id="bd4f9-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span></span>
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span data-ttu-id="bd4f9-131"><span id="winrm"></span><span id="WINRM"></span>WinRM</span><span class="sxs-lookup"><span data-stu-id="bd4f9-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="bd4f9-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span><span class="sxs-lookup"><span data-stu-id="bd4f9-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="bd4f9-133"><span id="shell"></span><span id="SHELL"></span>interfaz</span><span class="sxs-lookup"><span data-stu-id="bd4f9-133"><span id="shell"></span><span id="SHELL"></span>shell</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="bd4f9-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd4f9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd4f9-135">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="bd4f9-135">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="bd4f9-136">Administración remota de Windows y WMI</span><span class="sxs-lookup"><span data-stu-id="bd4f9-136">Windows Remote Management and WMI</span></span>](windows-remote-management-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="bd4f9-137">URI de recursos</span><span class="sxs-lookup"><span data-stu-id="bd4f9-137">Resource URIs</span></span>](resource-uris.md)
</dt> </dl>
