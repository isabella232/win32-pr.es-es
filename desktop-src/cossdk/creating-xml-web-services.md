---
description: Cualquier aplicación COM+ se puede exponer como un servicio Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Crear servicios Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705303"
---
# <a name="creating-xml-web-services"></a><span data-ttu-id="4367a-103">Crear servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="4367a-103">Creating XML Web Services</span></span>

<span data-ttu-id="4367a-104">Cualquier aplicación COM+ se puede exponer como un servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="4367a-104">Any COM+ application can be exposed as an XML web service.</span></span> <span data-ttu-id="4367a-105">A continuación, se puede llamar a los métodos de las interfaces predeterminadas de los componentes configurados de las aplicaciones (componentes en el catálogo COM+ de servidores) de forma remota.</span><span class="sxs-lookup"><span data-stu-id="4367a-105">The methods in the default interfaces of the applications configured components (components in the servers COM+ catalog) can then be called remotely.</span></span> <span data-ttu-id="4367a-106">Puede usar la herramienta administrativa Servicios de componentes para crear un directorio raíz virtual de IIS desde el que se puede llamar a los métodos de componente mediante SOAP.</span><span class="sxs-lookup"><span data-stu-id="4367a-106">You can use the Component Services administrative tool to create an IIS virtual root directory from which the component methods can be called by using SOAP.</span></span>

> [!Note]  
> <span data-ttu-id="4367a-107">El .NET Framework debe estar instalado en el equipo para poder exponer una aplicación COM+ como un servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="4367a-107">The .NET Framework must be installed on your computer in order to expose a COM+ application as an XML web service.</span></span>

 

<span data-ttu-id="4367a-108">**Para exponer una aplicación COM+ como un servicio Web XML**</span><span class="sxs-lookup"><span data-stu-id="4367a-108">**To expose a COM+ application as an XML web service**</span></span>

1.  <span data-ttu-id="4367a-109">En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.</span><span class="sxs-lookup"><span data-stu-id="4367a-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="4367a-110">Haga clic con el botón secundario en la aplicación que desea exponer como un servicio Web XML y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="4367a-110">Right-click the application you want to expose as an XML web service, and choose **Properties**.</span></span>

3.  <span data-ttu-id="4367a-111">Haga clic en la pestaña **activación** en el cuadro de diálogo Propiedades.</span><span class="sxs-lookup"><span data-stu-id="4367a-111">Click the **Activation** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="4367a-112">Active la casilla **usar SOAP** .</span><span class="sxs-lookup"><span data-stu-id="4367a-112">Select the **Uses SOAP** check box.</span></span>

5.  <span data-ttu-id="4367a-113">En el cuadro de texto **vroot de SOAP** , escriba el nombre del directorio raíz virtual de IIS desde el que se puede tener acceso a los métodos de los componentes de forma remota.</span><span class="sxs-lookup"><span data-stu-id="4367a-113">In the **SOAP VRoot** text box, enter the name of the IIS virtual root directory from which the components methods can be accessed remotely.</span></span> <span data-ttu-id="4367a-114">Tenga en cuenta que una VRoot de SOAP no puede ser un subdirectorio de otro directorio VRoot de SOAP.</span><span class="sxs-lookup"><span data-stu-id="4367a-114">Note that a SOAP VRoot cannot be a subdirectory of another SOAP VRoot directory.</span></span>

6.  <span data-ttu-id="4367a-115">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="4367a-115">Click **OK**.</span></span>

    <span data-ttu-id="4367a-116">Si especifica el directorio raíz virtual de IIS como *vroot* y si el nombre de dominio completo de los servidores es *ServerName*, la dirección URL donde se expone el componente como un servicio Web XML es https://*ServerName* / *vroot*/.</span><span class="sxs-lookup"><span data-stu-id="4367a-116">If you specify the IIS virtual root directory as *vroot* and if your servers fully qualified domain name is *servername*, the URL where your component is exposed as an XML web service is https://*servername*/*vroot*/.</span></span>

    <span data-ttu-id="4367a-117">El directorio correspondiente en el sistema de archivos es \\ Windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ; COM+ coloca en ella varios archivos de configuración y programas de ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="4367a-117">The corresponding directory in your file system is \\windows\\system32\\com\\SoapVRoots\\*vroot*\\; COM+ places several configuration files and ASP.NET programs there.</span></span> <span data-ttu-id="4367a-118">Para un servicio Web XML con mucha carga, es posible que desee ajustar los parámetros almacenados en el archivo web.config. Para obtener información acerca de este archivo, consulte la documentación de IIS.</span><span class="sxs-lookup"><span data-stu-id="4367a-118">For an XML web service under heavy load, you may want to adjust the parameters stored in the file web.config. For information about this file, consult the IIS documentation.</span></span>

    <span data-ttu-id="4367a-119">La configuración de seguridad predeterminada para una aplicación COM+ expuesta como un servicio Web XML varía en función de la versión de la .NET Framework esté instalada.</span><span class="sxs-lookup"><span data-stu-id="4367a-119">The default security settings for a COM+ application exposed as an XML web service differ depending on which version of the .NET Framework is installed.</span></span> <span data-ttu-id="4367a-120">Si está instalada la versión 1,0, los servicios Web XML no son seguros de forma predeterminada; todas las llamadas se aceptan y no se utiliza ningún cifrado.</span><span class="sxs-lookup"><span data-stu-id="4367a-120">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="4367a-121">Si está instalada la versión 1,1 o posterior, los servicios Web XML son seguros de forma predeterminada. los llamadores deben autenticarse y se requiere cifrado.</span><span class="sxs-lookup"><span data-stu-id="4367a-121">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4367a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4367a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4367a-123">Obtener acceso a los servicios Web XML en el modo de CAO</span><span class="sxs-lookup"><span data-stu-id="4367a-123">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="4367a-124">Obtener acceso a los servicios Web XML en modo WKO</span><span class="sxs-lookup"><span data-stu-id="4367a-124">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="4367a-125">Introducción al servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="4367a-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="4367a-126">Proteger los servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="4367a-126">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



