---
description: Usar archivos de configuración de Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Usar archivos de configuración de Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696108"
---
# <a name="using-per-application-configuration-files"></a><span data-ttu-id="153f4-103">Usar archivos de configuración de Per-Application</span><span class="sxs-lookup"><span data-stu-id="153f4-103">Using Per-Application Configuration Files</span></span>

<span data-ttu-id="153f4-104">El uso de archivos de configuración de COM+ por aplicación requiere los siguientes pasos básicos:</span><span class="sxs-lookup"><span data-stu-id="153f4-104">Using COM+ per-application configuration files requires the following basic steps:</span></span>

-   <span data-ttu-id="153f4-105">Configure un directorio raíz de la aplicación para una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="153f4-105">Configure an application root directory for a COM+ application.</span></span>
-   <span data-ttu-id="153f4-106">Cree archivos Application. manifest y application.config en el directorio raíz de la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="153f4-106">Create application.manifest and application.config files in the COM+ application root directory.</span></span>

> [!Note]  
> <span data-ttu-id="153f4-107">Los archivos de configuración por aplicación solo están disponibles a partir de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="153f4-107">Per-application configuration files are only available starting with Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span>

 

<span data-ttu-id="153f4-108">**Para usar un archivo de configuración por aplicación**</span><span class="sxs-lookup"><span data-stu-id="153f4-108">**To use a per-application configuration file**</span></span>

1.  <span data-ttu-id="153f4-109">Cree una biblioteca de clases .NET, con una referencia al ensamblado System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="153f4-109">Create a .NET class library, with a reference to the System.EnterpriseServices assembly.</span></span>

2.  <span data-ttu-id="153f4-110">La biblioteca de clases debe contener el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="153f4-110">The class library should contain the following code:</span></span>

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    <span data-ttu-id="153f4-111">Tenga en cuenta que "ConfigData1" es un nombre de configuración de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="153f4-111">Note that "ConfigData1" is a sample setting name.</span></span> <span data-ttu-id="153f4-112">Puede reemplazarlo por el nombre de la configuración que prefiera.</span><span class="sxs-lookup"><span data-stu-id="153f4-112">You can replace this with the setting name of your choice.</span></span>

3.  <span data-ttu-id="153f4-113">Cree una aplicación COM+ vacía.</span><span class="sxs-lookup"><span data-stu-id="153f4-113">Create an empty COM+ application.</span></span> <span data-ttu-id="153f4-114">Para obtener instrucciones sobre cómo hacerlo, vea [crear una nueva aplicación com+](creating-a-new-com--application.md).</span><span class="sxs-lookup"><span data-stu-id="153f4-114">For instructions on how to do this, see [Creating a New COM+ Application](creating-a-new-com--application.md).</span></span>
4.  <span data-ttu-id="153f4-115">Instale la biblioteca de clases que ha creado en la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="153f4-115">Install the class library you created into the COM+ application.</span></span> <span data-ttu-id="153f4-116">Para obtener instrucciones sobre cómo hacerlo, consulte [instalación de nuevos componentes](installing-new-components.md).</span><span class="sxs-lookup"><span data-stu-id="153f4-116">For instructions on how to do this, see [Installing New Components](installing-new-components.md).</span></span>
5.  <span data-ttu-id="153f4-117">En la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en la aplicación COM+ que creó y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="153f4-117">In the Component Services administrative tool, right-click the COM+ application you created and select **Properties**.</span></span>
6.  <span data-ttu-id="153f4-118">En el cuadro de diálogo **propiedades** , seleccione la pestaña **activación** .</span><span class="sxs-lookup"><span data-stu-id="153f4-118">In the **Properties** dialog box, select the **Activation** tab.</span></span>
7.  <span data-ttu-id="153f4-119">Asegúrese de que el **tipo de activación** está establecido en aplicación de **servidor**.</span><span class="sxs-lookup"><span data-stu-id="153f4-119">Make sure the **Activation type** is set to **Server application**.</span></span>
8.  <span data-ttu-id="153f4-120">En el cuadro de texto **directorio raíz** de la aplicación, escriba la ruta de acceso o busque el directorio en el que desea almacenar los archivos de configuración de la aplicación para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="153f4-120">In the **Application Root Directory** text box, enter the path or browse to the directory where you want to store your application configuration files for this application.</span></span>
9.  <span data-ttu-id="153f4-121">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="153f4-121">Click **OK**.</span></span>

    <span data-ttu-id="153f4-122">Tenga en cuenta que también puede especificar el directorio raíz de la aplicación COM+ a través de la propiedad ApplicationDirectory de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="153f4-122">Note that you can also specify the COM+ application root directory through the ApplicationDirectory property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="153f4-123">Para obtener más información, vea [**aplicaciones**](applications.md).</span><span class="sxs-lookup"><span data-stu-id="153f4-123">For more information, see [**Applications**](applications.md).</span></span>

10. <span data-ttu-id="153f4-124">En el directorio que eligió para almacenar los archivos de configuración de la aplicación, cree un archivo denominado *Application*. manifest.</span><span class="sxs-lookup"><span data-stu-id="153f4-124">In the directory you chose to store your application configuration files, create a file named *application*.manifest.</span></span> <span data-ttu-id="153f4-125">Con un editor de texto, agregue el siguiente texto a este archivo:</span><span class="sxs-lookup"><span data-stu-id="153f4-125">With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. <span data-ttu-id="153f4-126">En el mismo directorio, cree un archivo denominado *Application*. config. Con un editor de texto, agregue el siguiente texto a este archivo:</span><span class="sxs-lookup"><span data-stu-id="153f4-126">In the same directory, create a file named *application*.config. With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    <span data-ttu-id="153f4-127">Tenga en cuenta que este archivo de configuración es solo un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="153f4-127">Note that this configuration file is just an example.</span></span> <span data-ttu-id="153f4-128">Puede crear varias claves con distintos nombres y valores.</span><span class="sxs-lookup"><span data-stu-id="153f4-128">You can create multiple keys with different names and values.</span></span> <span data-ttu-id="153f4-129">Sin embargo, tenga en cuenta que "ConfigData1" coincide con el nombre de la configuración usado en la biblioteca de clases creada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="153f4-129">Note, however, that "ConfigData1" matches the setting name used in the class library created earlier.</span></span>

12. <span data-ttu-id="153f4-130">Cree una aplicación de consola de .NET, con una referencia a la biblioteca de clases .NET que creó anteriormente, y una referencia al ensamblado System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="153f4-130">Create a .NET console application, with a reference to the .NET class library you created earlier, and a reference to the System.EnterpriseServices assembly.</span></span>
13. <span data-ttu-id="153f4-131">La aplicación de consola debe contener el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="153f4-131">The console application should contain the following code:</span></span>
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

<span data-ttu-id="153f4-132">Ejecución de la aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="153f4-132">Run the console application.</span></span> <span data-ttu-id="153f4-133">La salida debe ser:</span><span class="sxs-lookup"><span data-stu-id="153f4-133">The output should be:</span></span>

``` syntax
Configuration Data Number 1
```

 

 



