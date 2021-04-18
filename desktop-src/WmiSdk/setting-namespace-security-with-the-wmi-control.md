---
description: El control WMI es un complemento MMC que se encuentra en el panel de control y se usa para establecer la seguridad del espacio de nombres WMI manualmente en un equipo local. También puede establecer el espacio de nombres predeterminado para el scripting.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Establecer la seguridad del espacio de nombres con el control WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707269"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a><span data-ttu-id="646d0-104">Establecer la seguridad del espacio de nombres con el control WMI</span><span class="sxs-lookup"><span data-stu-id="646d0-104">Setting Namespace Security with the WMI Control</span></span>

<span data-ttu-id="646d0-105">El control WMI es un complemento MMC que se encuentra en el **Panel de control** y se usa para establecer la seguridad del espacio de nombres WMI manualmente en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="646d0-105">The WMI Control is an MMC snap-in located in the **Control Panel** and is used to set WMI namespace security manually on a local computer.</span></span> <span data-ttu-id="646d0-106">También puede establecer el espacio de nombres predeterminado para el scripting.</span><span class="sxs-lookup"><span data-stu-id="646d0-106">You can also set the default namespace for scripting.</span></span>


<span data-ttu-id="646d0-107">En el procedimiento siguiente se describe cómo localizar el control WMI.</span><span class="sxs-lookup"><span data-stu-id="646d0-107">The following procedure describes how to locate the WMI Control.</span></span>

<span data-ttu-id="646d0-108">**Para buscar el control WMI**</span><span class="sxs-lookup"><span data-stu-id="646d0-108">**To locate the WMI control**</span></span>

1.  <span data-ttu-id="646d0-109">En el **Panel de control**, haga doble clic en **herramientas administrativas**.</span><span class="sxs-lookup"><span data-stu-id="646d0-109">In the **Control Panel**, double-click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="646d0-110">En la ventana **Herramientas administrativas**, haga doble clic en **Administración de equipos**.</span><span class="sxs-lookup"><span data-stu-id="646d0-110">In the **Administrative Tools** window, double-click **Computer Management**.</span></span>
3.  <span data-ttu-id="646d0-111">En la ventana **Administración de equipos** , expanda el árbol **servicios y aplicaciones** y haga doble clic en el **control WMI**.</span><span class="sxs-lookup"><span data-stu-id="646d0-111">In the **Computer Management** window, expand the **Services and Applications** tree and double-click the **WMI Control**.</span></span>
4.  <span data-ttu-id="646d0-112">Haga clic con el botón secundario en el icono **control WMI** y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="646d0-112">Right-click the **WMI Control** icon and select **Properties**.</span></span>

<span data-ttu-id="646d0-113">En el procedimiento siguiente se describe cómo usar el control WMI para configurar la seguridad de un espacio de nombres como una plantilla y, a continuación, obtener mediante programación la configuración de seguridad para establecer la seguridad de otros espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="646d0-113">The following procedure describes how to use the WMI control to set up the security for a namespace as a template, then programmatically obtain the security settings to set security for other namespaces.</span></span>

<span data-ttu-id="646d0-114">**Para establecer la seguridad del espacio de nombres con el control WMI**</span><span class="sxs-lookup"><span data-stu-id="646d0-114">**To set namespace security with the WMI control**</span></span>

1.  <span data-ttu-id="646d0-115">Cree un nuevo espacio de nombres mediante el código de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="646d0-115">Create a new namespace by using Managed Object Format (MOF) code.</span></span>
2.  <span data-ttu-id="646d0-116">Ejecute el control WMI para establecer la seguridad en el nuevo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="646d0-116">Run the WMI Control to set the security on the new namespace.</span></span> <span data-ttu-id="646d0-117">En el menú **Inicio** , haga clic en **Ejecutar** y escriba **Wmimgmt. msc** o vea [localizar el control WMI](#).</span><span class="sxs-lookup"><span data-stu-id="646d0-117">On the **Start** menu, click **Run** and type **wmimgmt.msc** or see [Locating the WMI Control](#).</span></span>
3.  <span data-ttu-id="646d0-118">En el panel **control WMI** , haga clic con el botón secundario en **control WMI**, seleccione **propiedades** y, a continuación, seleccione la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="646d0-118">In the **WMI Control** pane, right-click **WMI Control**, choose **Properties**, and then select the **Security** tab.</span></span>
4.  <span data-ttu-id="646d0-119">Navegue al nuevo espacio de nombres, haga clic en **seguridad** y, a continuación, configure los grupos y permisos para el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="646d0-119">Navigate to the new namespace, click **Security**, and then configure groups and permissions for the namespace.</span></span>

<span data-ttu-id="646d0-120">También puede usar Instrumental de administración de Windows Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) para establecer la seguridad de los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="646d0-120">You can also use Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) to set namespace security.</span></span> <span data-ttu-id="646d0-121">Para obtener más información, vea [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="646d0-121">For more information, see [**wmic**](wmic.md).</span></span>

## <a name="setting-the-default-namespace-for-scripts"></a><span data-ttu-id="646d0-122">Establecer el espacio de nombres predeterminado para los scripts</span><span class="sxs-lookup"><span data-stu-id="646d0-122">Setting the Default Namespace for Scripts</span></span>

<span data-ttu-id="646d0-123">Si un script no se conecta explícitamente a un espacio de nombres al conectarse a WMI, WMI utiliza el espacio de nombres predeterminado especificado en este control.</span><span class="sxs-lookup"><span data-stu-id="646d0-123">If a script does not connect explicitly to a namespace when connecting to WMI, then WMI uses the default namespace specified in this control.</span></span> <span data-ttu-id="646d0-124">El valor predeterminado también se encuentra en la entrada del registro de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="646d0-124">The default is also found in the registry entry as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

<span data-ttu-id="646d0-125">Dado que el espacio de nombres predeterminado es fácil de cambiar, ya sea con este control o mediante programación llamando a los métodos de [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), especifique el espacio de nombres al conectarse a WMI a través del [moniker](constructing-a-moniker-string.md) o llamadas a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="646d0-125">Because the default namespace is easy to change, either with this control or programmatically by calling methods of [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specify the namespace when connecting to WMI either through the [moniker](constructing-a-moniker-string.md) or calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="646d0-126">Para obtener más información, consulte [crear un script WMI](creating-a-wmi-script.md) .</span><span class="sxs-lookup"><span data-stu-id="646d0-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md)</span></span>

<span data-ttu-id="646d0-127">**Para establecer el espacio de nombres predeterminado para los scripts**</span><span class="sxs-lookup"><span data-stu-id="646d0-127">**To set the default namespace for scripts**</span></span>

1.  <span data-ttu-id="646d0-128">En la ventana **propiedades de control WMI** , elija la pestaña **Opciones avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="646d0-128">In the **WMI Control Properties** window, choose the **Advanced** tab.</span></span>
2.  <span data-ttu-id="646d0-129">Haga clic en el botón **cambiar** y seleccione el espacio de nombres para establecer el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="646d0-129">Click the **Change** button and select the namespace to make the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="646d0-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="646d0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="646d0-131">Configuración de descriptores de seguridad de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="646d0-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
