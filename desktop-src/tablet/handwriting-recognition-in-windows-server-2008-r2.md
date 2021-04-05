---
description: Windows Server 2008 R2 agrega compatibilidad para el reconocimiento de escritura a mano del lado servidor a Windows. En este tema se describe cómo reconocer la escritura a mano en Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Reconocimiento de escritura a mano en Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078567"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a><span data-ttu-id="dd659-104">Reconocimiento de escritura a mano en Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dd659-104">Handwriting Recognition in Windows Server 2008 R2</span></span>

<span data-ttu-id="dd659-105">Windows Server 2008 R2 admite el reconocimiento de escritura a mano del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="dd659-105">Windows Server 2008 R2 supports server-side handwriting recognition.</span></span> <span data-ttu-id="dd659-106">El reconocimiento del lado servidor permite que un servidor reconozca el contenido de la entrada manuscrita en páginas Web.</span><span class="sxs-lookup"><span data-stu-id="dd659-106">Server-side recognition lets a server recognize content from pen input on Web pages.</span></span> <span data-ttu-id="dd659-107">Esto es especialmente útil cuando los usuarios de una red van a especificar términos que se interpretan con un diccionario personalizado.</span><span class="sxs-lookup"><span data-stu-id="dd659-107">This is particularly useful when users on a network will be specifying terms that are interpreted using a custom dictionary.</span></span> <span data-ttu-id="dd659-108">Por ejemplo, si tuviera una aplicación médica que consultase una base de datos del servidor para los nombres de los pacientes, estos nombres podrían agregarse a otra base de datos a la que se haría referencia cruzada al realizar búsquedas desde un formulario de Silverlight escrito a mano.</span><span class="sxs-lookup"><span data-stu-id="dd659-108">For example, if you had a medical application that queried a server database for patient names, those names could be added to another database that would be cross-referenced when performing searches from a handwritten Silverlight form.</span></span>

## <a name="set-up-your-server-for-server-side-recognition"></a><span data-ttu-id="dd659-109">Configuración del servidor para el reconocimiento de Server-Side</span><span class="sxs-lookup"><span data-stu-id="dd659-109">Set up your Server for Server-Side Recognition</span></span>

<span data-ttu-id="dd659-110">Se deben seguir los pasos siguientes para configurar el reconocimiento del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="dd659-110">The following steps should be followed to set up server-side recognition.</span></span>

- <span data-ttu-id="dd659-111">Instalar Servicios de Escritura con lápiz y Escritura a mano</span><span class="sxs-lookup"><span data-stu-id="dd659-111">Install Ink and Handwriting Services</span></span>
- <span data-ttu-id="dd659-112">Instalar compatibilidad con servidor Web (IIS) y servidor de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="dd659-112">Install Support for Web Server (IIS) and Application Server</span></span>
- <span data-ttu-id="dd659-113">Habilitar el rol experiencia de escritorio</span><span class="sxs-lookup"><span data-stu-id="dd659-113">Enable the Desktop Experience Role</span></span>
- <span data-ttu-id="dd659-114">Iniciar el servicio de entrada de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="dd659-114">Start the Tablet PC Input Service</span></span>

### <a name="install-ink-and-handwriting-services"></a><span data-ttu-id="dd659-115">Instalar Servicios de Escritura con lápiz y Escritura a mano</span><span class="sxs-lookup"><span data-stu-id="dd659-115">Install Ink and Handwriting Services</span></span>

<span data-ttu-id="dd659-116">Para instalar los servicios de tinta y escritura a mano, abra el administrador del servidor haciendo clic en el icono administrador del servidor de la bandeja Inicio rápido.</span><span class="sxs-lookup"><span data-stu-id="dd659-116">To install Ink and Handwriting services, open the server manager by clicking the server manager icon from the Quick Launch tray.</span></span> <span data-ttu-id="dd659-117">En el menú **características** , haga clic en **Agregar características**.</span><span class="sxs-lookup"><span data-stu-id="dd659-117">From the **Features** menu, click **Add Features**.</span></span> <span data-ttu-id="dd659-118">Asegúrese de activar la casilla **servicios de escritura con lápiz y escritura a mano** .</span><span class="sxs-lookup"><span data-stu-id="dd659-118">Make sure that you select the **Ink and Handwriting Services** check box.</span></span> <span data-ttu-id="dd659-119">La siguiente imagen muestra el cuadro de diálogo **seleccionar características** con **servicios de escritura con lápiz y escritura a mano** seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dd659-119">The following image shows the **Select Features** dialog box with **Ink and Handwriting Services** selected.</span></span>

<span data-ttu-id="dd659-120">![Cuadro de diálogo Seleccionar características con la casilla servicios de tinta y escritura a mano activada](images/setup-server-1-ink-and-handwriting.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-120">![Select features dialog box with ink and handwriting services check box selected](images/setup-server-1-ink-and-handwriting.png)</span></span><br/>
<span data-ttu-id="dd659-121">*Cuadro de diálogo Seleccionar características con la casilla servicios de tinta y escritura a mano activada*</span><span class="sxs-lookup"><span data-stu-id="dd659-121">*Select features dialog box with ink and handwriting services check box selected*</span></span>

### <a name="installation-support-for-web-server-iis-and-application-server"></a><span data-ttu-id="dd659-122">Compatibilidad con la instalación de servidor Web (IIS) y servidor de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="dd659-122">Installation Support for Web Server (IIS) and Application Server</span></span>

<span data-ttu-id="dd659-123">Abra el administrador del servidor como hizo para el primer paso.</span><span class="sxs-lookup"><span data-stu-id="dd659-123">Open the server manager as you did for the first step.</span></span> <span data-ttu-id="dd659-124">A continuación, tendrá que agregar los roles servidor Web (IIS) y servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd659-124">Next, you will need to add the Web Server (IIS) and Application Server roles.</span></span> <span data-ttu-id="dd659-125">En el menú **roles** , haga clic en **Agregar roles**.</span><span class="sxs-lookup"><span data-stu-id="dd659-125">From the **Roles** menu, click **Add Roles**.</span></span> <span data-ttu-id="dd659-126">Aparece el Asistente para agregar roles.</span><span class="sxs-lookup"><span data-stu-id="dd659-126">The Add Roles wizard appears.</span></span> <span data-ttu-id="dd659-127">Haga clic en **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd659-127">Click **Next**.</span></span> <span data-ttu-id="dd659-128">Asegúrese de que el servidor de **aplicaciones** y el **servidor Web (IIS)** están seleccionados.</span><span class="sxs-lookup"><span data-stu-id="dd659-128">Make sure **Application Server** and **Web Server (IIS)** are selected.</span></span> <span data-ttu-id="dd659-129">La siguiente imagen muestra el cuadro de diálogo **Seleccionar roles de servidor** con los roles **servidor Web (IIS)** y **servidor de aplicaciones** seleccionados.</span><span class="sxs-lookup"><span data-stu-id="dd659-129">The following image shows the **Select Server Roles** dialog box with the **Web Server (IIS)** and **Application Server** roles selected.</span></span>

<span data-ttu-id="dd659-130">![Cuadro de diálogo Seleccionar roles de servidor con los roles servidor Web (IIS) y servidor de aplicaciones seleccionados](images/setup-server-2-select-server-roles.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-130">![Select server roles dialog box with web server (iis) and application server roles selected](images/setup-server-2-select-server-roles.png)</span></span><br/>
<span data-ttu-id="dd659-131">*Cuadro de diálogo Seleccionar roles de servidor con los roles servidor Web (IIS) y servidor de aplicaciones seleccionados*</span><span class="sxs-lookup"><span data-stu-id="dd659-131">*Select server roles dialog box with web server (iis) and application server roles selected*</span></span>

<span data-ttu-id="dd659-132">Al seleccionar **servidor de aplicaciones**, se le pedirá que instale el marco de trabajo de ASP.net.</span><span class="sxs-lookup"><span data-stu-id="dd659-132">When you select **Application Server**, you will be asked to install the ASP.NET framework.</span></span> <span data-ttu-id="dd659-133">Haga clic en el botón **Agregar las características necesarias** .</span><span class="sxs-lookup"><span data-stu-id="dd659-133">Click the **Add the Required Features** button.</span></span> <span data-ttu-id="dd659-134">Después de hacer clic en **siguiente**, aparecerá un cuadro de diálogo de información general. Haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="dd659-134">After you click **Next**, you will be presented with an overview dialog box; click **Next**.</span></span> <span data-ttu-id="dd659-135">Ahora debe estar disponible el cuadro de diálogo **seleccionar servicios de rol** .</span><span class="sxs-lookup"><span data-stu-id="dd659-135">The **Select Role Services** dialog box should now be available.</span></span> <span data-ttu-id="dd659-136">Asegúrese de que el **servidor Web (IIS)** está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dd659-136">Make sure that **Web Server (IIS)** is selected.</span></span> <span data-ttu-id="dd659-137">La siguiente imagen muestra el cuadro de diálogo **seleccionar servicios de rol** con el servidor Web (IIS) habilitado.</span><span class="sxs-lookup"><span data-stu-id="dd659-137">The following image shows the **Select Role Services** dialog box with Web Server (IIS) enabled.</span></span>

<span data-ttu-id="dd659-138">![Cuadro de diálogo Seleccionar servicios de rol con el servidor Web (IIS) habilitado](images/setup-server-3-select-role-services.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-138">![Select role services dialog box with web server (iis) enabled](images/setup-server-3-select-role-services.png)</span></span><br/>
<span data-ttu-id="dd659-139">*Cuadro de diálogo Seleccionar servicios de rol con el servidor Web (IIS) habilitado*</span><span class="sxs-lookup"><span data-stu-id="dd659-139">*Select role services dialog box with web server (iis) enabled*</span></span>

<span data-ttu-id="dd659-140">Haga clic en **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd659-140">Click **Next**.</span></span> <span data-ttu-id="dd659-141">Aparece un cuadro de diálogo de información general; Vuelva a hacer clic en **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="dd659-141">An overview dialog box appears; click **Next** again.</span></span> <span data-ttu-id="dd659-142">Ahora se le presentará una página que le ofrece opciones para los roles de servidor Web (IIS).</span><span class="sxs-lookup"><span data-stu-id="dd659-142">You will now be presented with a page offering you options for roles for Web Server (IIS).</span></span> <span data-ttu-id="dd659-143">Haga clic en **Next**.</span><span class="sxs-lookup"><span data-stu-id="dd659-143">Click **Next**.</span></span> <span data-ttu-id="dd659-144">En la página siguiente, el botón **instalar** se convertirá en activo.</span><span class="sxs-lookup"><span data-stu-id="dd659-144">On the next page, the **Install** button will become active.</span></span> <span data-ttu-id="dd659-145">Haga clic en **instalar** y podrá instalar la compatibilidad con servidor Web (IIS) y servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd659-145">Click **Install** and you will install support for Web Server (IIS) and Application Server.</span></span>

### <a name="enable-the-desktop-experience-role"></a><span data-ttu-id="dd659-146">Habilitar el rol experiencia de escritorio</span><span class="sxs-lookup"><span data-stu-id="dd659-146">Enable the Desktop Experience Role</span></span>

<span data-ttu-id="dd659-147">Para habilitar la experiencia de escritorio, haga clic en **Inicio**, en **herramientas administrativas** y, a continuación, en **Administrador del servidor**.</span><span class="sxs-lookup"><span data-stu-id="dd659-147">To enable the desktop experience, click **Start**, click **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="dd659-148">Seleccione **Agregar servicios** y, a continuación, seleccione el servicio **experiencia de escritorio** .</span><span class="sxs-lookup"><span data-stu-id="dd659-148">Select **Add Services** and then select the **Desktop Experience** service.</span></span> <span data-ttu-id="dd659-149">La siguiente imagen muestra el cuadro de diálogo **seleccionar características** con el elemento experiencia de escritorio instalado.</span><span class="sxs-lookup"><span data-stu-id="dd659-149">The following image shows the **Select Features** dialog box with the Desktop Experience item installed.</span></span>

<span data-ttu-id="dd659-150">![Cuadro de diálogo Seleccionar características con el servicio experiencia de escritorio seleccionado](images/setup-server-4-desktop-experience.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-150">![Select features dialog box with desktop experience service selected](images/setup-server-4-desktop-experience.png)</span></span><br/>
<span data-ttu-id="dd659-151">*Cuadro de diálogo Seleccionar características con el servicio experiencia de escritorio seleccionado*</span><span class="sxs-lookup"><span data-stu-id="dd659-151">*Select features dialog box with desktop experience service selected*</span></span>

<span data-ttu-id="dd659-152">Haga clic en **siguiente** para instalar la experiencia de escritorio.</span><span class="sxs-lookup"><span data-stu-id="dd659-152">Click **Next** to install the Desktop Experience.</span></span>

### <a name="start-the-tablet-service"></a><span data-ttu-id="dd659-153">Iniciar el servicio de tableta</span><span class="sxs-lookup"><span data-stu-id="dd659-153">Start the Tablet Service</span></span>

<span data-ttu-id="dd659-154">Una vez instalado el servicio de experiencia de escritorio, el servicio de entrada de Tablet PC aparecerá en el menú **servicios** .</span><span class="sxs-lookup"><span data-stu-id="dd659-154">After you have installed the Desktop Experience service, the Tablet PC Input service will appear in the **Services** menu.</span></span> <span data-ttu-id="dd659-155">Para tener acceso al menú **servicios** , haga clic en **Inicio**, en **herramientas administrativas** y, a continuación, haga clic en **servicios**.</span><span class="sxs-lookup"><span data-stu-id="dd659-155">To access the **Services** menu, click **Start**, click **Administrative Tools**, and then click **Services**.</span></span> <span data-ttu-id="dd659-156">Para iniciar el servicio, haga clic con el botón secundario en **servicio de entrada de Tablet PC** y, a continuación, haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="dd659-156">To start the service, right-click **Tablet PC Input Service** and then click **Start**.</span></span> <span data-ttu-id="dd659-157">La imagen siguiente muestra el menú **servicios** con el servicio de entrada de Tablet PC iniciado.</span><span class="sxs-lookup"><span data-stu-id="dd659-157">The following image shows the **Services** menu with the Tablet PC Input Service started.</span></span>

<span data-ttu-id="dd659-158">![Menú servicios con el servicio de entrada de Tablet PC iniciado](images/setup-server-5-tablet-pc-input-service.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-158">![Services menu with the tablet pc input service started](images/setup-server-5-tablet-pc-input-service.png)</span></span><br/>
<span data-ttu-id="dd659-159">*Menú servicios con el servicio de entrada de Tablet PC iniciado*</span><span class="sxs-lookup"><span data-stu-id="dd659-159">*Services menu with the tablet pc input service started*</span></span>

## <a name="performing-server-side-recognition-using-silverlight"></a><span data-ttu-id="dd659-160">Realización del reconocimiento de Server-Side con Silverlight</span><span class="sxs-lookup"><span data-stu-id="dd659-160">Performing Server-Side Recognition Using Silverlight</span></span>

<span data-ttu-id="dd659-161">En esta sección se muestra cómo crear una aplicación web que usa Silverlight para capturar entradas de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="dd659-161">This section shows how to create a Web application that uses Silverlight to capture handwriting input.</span></span> <span data-ttu-id="dd659-162">Siga los pasos que se indican a continuación para programar el reconocedor en Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="dd659-162">Use the following steps to program the recognizer in Visual Studio 2008.</span></span>

- <span data-ttu-id="dd659-163">Instale y actualice Visual Studio 2008 para agregar compatibilidad con Silverlight.</span><span class="sxs-lookup"><span data-stu-id="dd659-163">Install and update Visual Studio 2008 to add support for Silverlight.</span></span>
- <span data-ttu-id="dd659-164">Cree un nuevo proyecto de Silverlight en Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="dd659-164">Create a new Silverlight project in Visual Studio 2008.</span></span>
- <span data-ttu-id="dd659-165">Agregue las referencias de servicio necesarias al proyecto.</span><span class="sxs-lookup"><span data-stu-id="dd659-165">Add the necessary service references to your project.</span></span>
- <span data-ttu-id="dd659-166">Cree un servicio WCF de Silverlight para el reconocimiento de tinta.</span><span class="sxs-lookup"><span data-stu-id="dd659-166">Create a Silverlight WCF Service for ink recognition.</span></span>
- <span data-ttu-id="dd659-167">Agregue la referencia de servicio al proyecto de cliente.</span><span class="sxs-lookup"><span data-stu-id="dd659-167">Add the service reference to your client project.</span></span>
- <span data-ttu-id="dd659-168">Agregue la clase InkCollector al proyecto InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="dd659-168">Add the InkCollector class to the InkRecognition project.</span></span>
- <span data-ttu-id="dd659-169">Quitar directivas de transporte seguro de la configuración del cliente</span><span class="sxs-lookup"><span data-stu-id="dd659-169">Remove secure transport directives from the client configuration</span></span>

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a><span data-ttu-id="dd659-170">Instalación y actualización de Visual Studio 2008 para agregar compatibilidad con Silverlight</span><span class="sxs-lookup"><span data-stu-id="dd659-170">Install and Update Visual Studio 2008 to Add Support for Silverlight</span></span>

<span data-ttu-id="dd659-171">Antes de comenzar, debe realizar los siguientes pasos en el servidor de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="dd659-171">Before you begin, you must perform the following steps on your Windows Server 2008 R2 server.</span></span>

- <span data-ttu-id="dd659-172">Instale Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="dd659-172">Install Visual Studio 2008.</span></span>
- <span data-ttu-id="dd659-173">Instale [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span><span class="sxs-lookup"><span data-stu-id="dd659-173">Install [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span></span>
- <span data-ttu-id="dd659-174">Instale el [SDK de Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).</span><span class="sxs-lookup"><span data-stu-id="dd659-174">Install [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span></span>

<span data-ttu-id="dd659-175">Después de instalar estas aplicaciones y actualizaciones, está listo para crear la aplicación Web de reconocimiento del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="dd659-175">After you have installed these applications and updates, you are ready to create your server-side recognition Web application.</span></span>

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a><span data-ttu-id="dd659-176">Crear un nuevo proyecto Web de Silverlight en Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="dd659-176">Create a new Silverlight Web Project in Visual Studio 2008</span></span>

<span data-ttu-id="dd659-177">En el menú **Archivo**, haga clic en **Nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="dd659-177">From the **File** menu, click **New Project**.</span></span> <span data-ttu-id="dd659-178">Seleccione la plantilla aplicación de Silverlight en la lista proyecto de Visual C \# .</span><span class="sxs-lookup"><span data-stu-id="dd659-178">Select the Silverlight Application template from the Visual C\# project list.</span></span> <span data-ttu-id="dd659-179">Asigne al proyecto el nombre InkRecognition y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dd659-179">Name your project InkRecognition and click **OK**.</span></span> <span data-ttu-id="dd659-180">En la imagen siguiente se muestra el proyecto de Silverlight de C \# seleccionado y denominado InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="dd659-180">The following image shows the C\# Silverlight project selected and named InkRecognition.</span></span>

<span data-ttu-id="dd659-181">![proyecto de Silverlight de c \# seleccionado, con el nombre InkRecognition](images/project-1-new-project.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-181">![c\# silverlight project selected, with the name inkrecognition](images/project-1-new-project.png)</span></span><br/>
<span data-ttu-id="dd659-182">*proyecto de Silverlight de c \# seleccionado, con el nombre InkRecognition*</span><span class="sxs-lookup"><span data-stu-id="dd659-182">*c\# silverlight project selected, with the name inkrecognition*</span></span>

<span data-ttu-id="dd659-183">Después de hacer clic en **Aceptar**, un cuadro de diálogo le pedirá que agregue una aplicación de Silverlight al proyecto.</span><span class="sxs-lookup"><span data-stu-id="dd659-183">After you click **OK**, a dialog box prompts you to add a Silverlight application to your project.</span></span> <span data-ttu-id="dd659-184">Seleccione **Agregar un nuevo proyecto Web ASP.net a la solución para hospedar Silverlight** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dd659-184">Select **Add a new ASP.NET Web project to the solution to host Silverlight** and click **OK**.</span></span> <span data-ttu-id="dd659-185">En la imagen siguiente se muestra cómo configurar el proyecto de ejemplo antes de hacer clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dd659-185">The following image shows how to set up the example project before you click **OK**.</span></span>

<span data-ttu-id="dd659-186">![Cuadro de diálogo con el símbolo del sistema para agregar una aplicación de Silverlight a un proyecto](images/project-2-add-a-new-aspnetproject.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-186">![Dialog box with prompt for adding a silverlight application to a project](images/project-2-add-a-new-aspnetproject.png)</span></span><br/>
<span data-ttu-id="dd659-187">*Cuadro de diálogo con el símbolo del sistema para agregar una aplicación de Silverlight a un proyecto*</span><span class="sxs-lookup"><span data-stu-id="dd659-187">*Dialog box with prompt for adding a silverlight application to a project*</span></span>

### <a name="add-the-necessary-service-references-to-your-project"></a><span data-ttu-id="dd659-188">Agregue las referencias de servicio necesarias al proyecto</span><span class="sxs-lookup"><span data-stu-id="dd659-188">Add the Necessary Service References to your Project</span></span>

<span data-ttu-id="dd659-189">Ahora tiene un proyecto de cliente de Silverlight genérico (InkRecognition) con un proyecto web (InkRecognition. Web) configurado en la solución.</span><span class="sxs-lookup"><span data-stu-id="dd659-189">Now you have your generic Silverlight client project (InkRecognition) with a Web project (InkRecognition.Web) set up in your solution.</span></span> <span data-ttu-id="dd659-190">El proyecto se abrirá con Page. XAML y default. aspx abierto.</span><span class="sxs-lookup"><span data-stu-id="dd659-190">The project will open with Page.xaml and Default.aspx open.</span></span> <span data-ttu-id="dd659-191">Cierre estas ventanas y agregue las referencias System. Runtime. Serialization y System. ServiceModel al proyecto InkRecognition haciendo clic con el botón derecho en la carpeta referencias del proyecto InkRecognition y seleccionando **Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="dd659-191">Close these windows and add the System.Runtime.Serialization and System.ServiceModel references to the InkRecognition project by right-clicking on the references folder in the InkRecognition project and selecting **Add Reference**.</span></span> <span data-ttu-id="dd659-192">La siguiente imagen muestra el cuadro de diálogo con las referencias de requisitos seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="dd659-192">The following image shows the dialog box with the requisite references selected.</span></span>

<span data-ttu-id="dd659-193">![Cuadro de diálogo Agregar referencias con System. Runtime. Serialization y System. ServiceModel seleccionado](images/project-3a-add-references-to-inkreco.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-193">![Add references dialog box with system.runtime.serialization and system.servicemodel selected](images/project-3a-add-references-to-inkreco.png)</span></span><br/>
<span data-ttu-id="dd659-194">*Cuadro de diálogo Agregar referencias con System. Runtime. Serialization y System. ServiceModel seleccionado*</span><span class="sxs-lookup"><span data-stu-id="dd659-194">*Add references dialog box with system.runtime.serialization and system.servicemodel selected*</span></span>

<span data-ttu-id="dd659-195">A continuación, debe agregar las referencias a System. ServiceModel y Microsoft. Ink al proyecto InkRecognition. Web.</span><span class="sxs-lookup"><span data-stu-id="dd659-195">Next, you need to add the System.ServiceModel and Microsoft.Ink references to the InkRecognition.Web project.</span></span> <span data-ttu-id="dd659-196">La referencia de Microsoft. Ink no aparecerá en las referencias de .NET de forma predeterminada, por lo que busque Microsoft.Ink.dll en la carpeta de Windows.</span><span class="sxs-lookup"><span data-stu-id="dd659-196">The Microsoft.Ink reference will not appear in the .NET references by default, so search your Windows folder for Microsoft.Ink.dll.</span></span> <span data-ttu-id="dd659-197">Una vez localizado el archivo DLL, agregue el ensamblado a las referencias del proyecto: seleccione la pestaña **examinar** , cambie a la carpeta que contiene Microsoft.Ink.dll, seleccione Microsoft.Ink.dll y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dd659-197">After you have located the DLL, add the assembly to the project references: select the **Browse** tab, change to the folder containing Microsoft.Ink.dll, select Microsoft.Ink.dll, and then click **OK**.</span></span> <span data-ttu-id="dd659-198">La siguiente imagen muestra la solución del proyecto en el explorador de Windows con todos los ensamblados de referencia agregados.</span><span class="sxs-lookup"><span data-stu-id="dd659-198">The following image shows the project's solution in Windows Explorer with all of the reference assemblies added.</span></span>

<span data-ttu-id="dd659-199">![proyecto InkRecognition en el explorador de Windows con todos los ensamblados de referencia agregados](images/project-3b-with-reference-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-199">![inkrecognition project in windows explorer with all reference assemblies added](images/project-3b-with-reference-assemblies.png)</span></span><br/>
<span data-ttu-id="dd659-200">*proyecto InkRecognition en el explorador de Windows con todos los ensamblados de referencia agregados*</span><span class="sxs-lookup"><span data-stu-id="dd659-200">*inkrecognition project in windows explorer with all reference assemblies added*</span></span>

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a><span data-ttu-id="dd659-201">Crear un servicio WCF de Silverlight para el reconocimiento de tinta</span><span class="sxs-lookup"><span data-stu-id="dd659-201">Create a Silverlight WCF Service for Ink Recognition</span></span>

<span data-ttu-id="dd659-202">A continuación, agregará un servicio WCF para el reconocimiento de entradas manuscritas en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="dd659-202">Next, you will add a WCF service for ink recognition to the project.</span></span> <span data-ttu-id="dd659-203">Haga clic con el botón derecho en el proyecto InkRecognition. Web, haga clic en **Agregar** y, a continuación, haga clic en **nuevo elemento**.</span><span class="sxs-lookup"><span data-stu-id="dd659-203">Right-click your InkRecognition.Web project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="dd659-204">Seleccione la plantilla de servicio WCF Silverlight, cambie el nombre a InkRecogitionService y, a continuación, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="dd659-204">Select the WCF Silverlight Service template, change the name to InkRecogitionService, and then click **Add**.</span></span> <span data-ttu-id="dd659-205">La siguiente imagen muestra el cuadro de diálogo **Agregar nuevo elemento** con el servicio WCF de Silverlight seleccionado y denominado.</span><span class="sxs-lookup"><span data-stu-id="dd659-205">The following image shows the **Add New Item** dialog box with the Silverlight WCF service selected and named.</span></span>

<span data-ttu-id="dd659-206">![Cuadro de diálogo Agregar nuevo elemento con el servicio WCF de Silverlight seleccionado y con nombre](images/project-4-add-wcf-service.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-206">![Add new item dialog box with silverlight wcf service selected and named](images/project-4-add-wcf-service.png)</span></span><br/>
<span data-ttu-id="dd659-207">*Cuadro de diálogo Agregar nuevo elemento con el servicio WCF de Silverlight seleccionado y con nombre*</span><span class="sxs-lookup"><span data-stu-id="dd659-207">*Add new item dialog box with silverlight wcf service selected and named*</span></span>

<span data-ttu-id="dd659-208">Después de agregar el servicio WCF Silverlight, se abrirá el código de servicio subyacente, InkRecognitionService. cs.</span><span class="sxs-lookup"><span data-stu-id="dd659-208">After you add the WCF Silverlight service, the service code behind, InkRecognitionService.cs, will open.</span></span> <span data-ttu-id="dd659-209">Reemplace el código del servicio por el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd659-209">Replace the service code with the following code.</span></span>

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a><span data-ttu-id="dd659-210">Agregar la referencia de servicio al proyecto de cliente</span><span class="sxs-lookup"><span data-stu-id="dd659-210">Add the Service Reference to your Client Project</span></span>

<span data-ttu-id="dd659-211">Ahora que tiene el servicio WCF de Silverlight para InkRecognition, consumirá el servicio desde la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="dd659-211">Now that you have your Silverlight WCF service for InkRecognition, you will consume the service from your client application.</span></span> <span data-ttu-id="dd659-212">Haga clic con el botón derecho en el proyecto InkRecognition y seleccione **Agregar referencia de servicio**.</span><span class="sxs-lookup"><span data-stu-id="dd659-212">Right-click the InkRecognition project and select **Add Service Reference**.</span></span> <span data-ttu-id="dd659-213">En el cuadro de diálogo **Agregar referencia de servicio** que aparece, seleccione **detectar** para detectar los servicios de la solución actual.</span><span class="sxs-lookup"><span data-stu-id="dd659-213">From the **Add Service Reference** dialog box that appears, select **Discover** to discover services from the current solution.</span></span> <span data-ttu-id="dd659-214">InkRecognitionService aparecerá en el panel servicios.</span><span class="sxs-lookup"><span data-stu-id="dd659-214">InkRecognitionService will appear in the Services pane.</span></span> <span data-ttu-id="dd659-215">Haga doble clic en InkRecognitionService en el panel servicios, cambie el espacio de nombres a InkRecognitionServiceReference y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dd659-215">Double-click InkRecognitionService from the Services pane, change the namespace to InkRecognitionServiceReference, and then click **OK**.</span></span> <span data-ttu-id="dd659-216">La siguiente imagen muestra el cuadro de diálogo **Agregar referencia de servicio** con InkRecognitionService seleccionado y el espacio de nombres cambiado.</span><span class="sxs-lookup"><span data-stu-id="dd659-216">The following image shows the **Add Service Reference** dialog box with InkRecognitionService selected and the namespace changed.</span></span>

<span data-ttu-id="dd659-217">![Cuadro de diálogo Agregar referencia de servicio con el inkrecognitionservice seleccionado y el espacio de nombres cambiado](images/project-5-discover-service-reference.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-217">![Add service reference dialog box with inkrecognitionservice selected and namespace changed](images/project-5-discover-service-reference.png)</span></span><br/>
<span data-ttu-id="dd659-218">*Cuadro de diálogo Agregar referencia de servicio con el inkrecognitionservice seleccionado y el espacio de nombres cambiado*</span><span class="sxs-lookup"><span data-stu-id="dd659-218">*Add service reference dialog box with inkrecognitionservice selected and namespace changed*</span></span>

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a><span data-ttu-id="dd659-219">Agregue la clase InkCollector al proyecto InkRecognition</span><span class="sxs-lookup"><span data-stu-id="dd659-219">Add the InkCollector Class to the InkRecognition Project</span></span>

<span data-ttu-id="dd659-220">Haga clic con el botón secundario en el proyecto InkRecognition, haga clic en **Agregar** y, a continuación, haga clic en **nuevo elemento**.</span><span class="sxs-lookup"><span data-stu-id="dd659-220">Right-click the InkRecognition project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="dd659-221">En el menú de **Visual c \#** , **Seleccione \# clase c**.</span><span class="sxs-lookup"><span data-stu-id="dd659-221">From the **Visual C\#** menu, select **C\# class**.</span></span> <span data-ttu-id="dd659-222">Asigne a la clase el nombre InkCollector.</span><span class="sxs-lookup"><span data-stu-id="dd659-222">Name the class InkCollector.</span></span> <span data-ttu-id="dd659-223">La siguiente imagen muestra el cuadro de diálogo con la \# clase C seleccionada y con el nombre.</span><span class="sxs-lookup"><span data-stu-id="dd659-223">The following image shows the dialog box with the C\# class selected and named.</span></span>

<span data-ttu-id="dd659-224">![Cuadro de diálogo Agregar nuevo elemento con la \# clase c seleccionada y con el nombre](images/project-6-add-ink-collector.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-224">![Add new item dialog box with c\# class selected and named](images/project-6-add-ink-collector.png)</span></span><br/>
<span data-ttu-id="dd659-225">*Cuadro de diálogo Agregar nuevo elemento con la \# clase c seleccionada y con el nombre*</span><span class="sxs-lookup"><span data-stu-id="dd659-225">*Add new item dialog box with c\# class selected and named*</span></span>

<span data-ttu-id="dd659-226">Después de agregar la clase InkCollector, se abrirá la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="dd659-226">After you add the InkCollector class, the class definition will open.</span></span> <span data-ttu-id="dd659-227">Reemplace el código del recopilador de tinta con el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd659-227">Replace the code in the Ink Collector with the following code.</span></span>

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a><span data-ttu-id="dd659-228">Actualizar el XAML de la página predeterminada y agregar un código subyacente para el reconocimiento de escritura a mano</span><span class="sxs-lookup"><span data-stu-id="dd659-228">Update the XAML for the Default Page and Add a Code Behind for Handwriting Recognition</span></span>

<span data-ttu-id="dd659-229">Ahora que tiene una clase que recopila entradas manuscritas, deberá actualizar el código XAML en Page. XAML con el código XAML siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd659-229">Now that you have a class that collects ink, you will need to update the XAML in page.xaml with the following XAML.</span></span> <span data-ttu-id="dd659-230">En el código siguiente se agrega un degradado amarillo al área de entrada, un control InkCanvas y un botón que desencadenará el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="dd659-230">The following code adds a yellow gradient to the input area, an InkCanvas control, and a button that will trigger recognition.</span></span>

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

<span data-ttu-id="dd659-231">Reemplace la página de código subyacente, Page. Xaml. CS, por el siguiente código que agregará un controlador de eventos para el botón **Recognize** .</span><span class="sxs-lookup"><span data-stu-id="dd659-231">Replace the code behind page, Page.xaml.cs, with the following code that will add an event handler for the **Recognize** button.</span></span>

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a><span data-ttu-id="dd659-232">Quitar directivas de transporte seguro de la configuración del cliente</span><span class="sxs-lookup"><span data-stu-id="dd659-232">Remove Secure Transport Directives from the Client Configuration</span></span>

<span data-ttu-id="dd659-233">Antes de que pueda consumir el servicio WCF, debe quitar todas las opciones de transporte seguro de la configuración del servicio, ya que los transportes seguros no se admiten actualmente en los servicios WCF de Silverlight 2,0.</span><span class="sxs-lookup"><span data-stu-id="dd659-233">Before you can consume the WCF service, you must remove all secure transport options from the service configuration because secure transports are not currently supported in Silverlight 2.0 WCF services.</span></span> <span data-ttu-id="dd659-234">En el proyecto InkRecognition, actualice la configuración de seguridad en ServiceReferences. ClientConfig.</span><span class="sxs-lookup"><span data-stu-id="dd659-234">From the InkRecognition project, update the security settings in ServiceReferences.ClientConfig.</span></span> <span data-ttu-id="dd659-235">Cambiar el código XML de seguridad de</span><span class="sxs-lookup"><span data-stu-id="dd659-235">Change the security XML from</span></span>

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

<span data-ttu-id="dd659-236">to</span><span class="sxs-lookup"><span data-stu-id="dd659-236">to</span></span>

```XML
       <security mode="None"/>
```

<span data-ttu-id="dd659-237">Ahora, la aplicación debe ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="dd659-237">Now, your application should run.</span></span> <span data-ttu-id="dd659-238">En la imagen siguiente se muestra el aspecto de la aplicación dentro de awebpagewith alguna escritura a mano escrita en el cuadro reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="dd659-238">The following image shows how the application looks within awebpagewith some handwriting entered into the recognition box.</span></span>

<span data-ttu-id="dd659-239">![Aplicación en awebpagewith alguna escritura a mano escrita en el cuadro de reconocimiento](images/demo-1.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-239">![Application within awebpagewith some handwriting entered into recognition box](images/demo-1.png)</span></span><br/>
<span data-ttu-id="dd659-240">*Aplicación en awebpagewith alguna escritura a mano escrita en el cuadro de reconocimiento*</span><span class="sxs-lookup"><span data-stu-id="dd659-240">*Application within awebpagewith some handwriting entered into recognition box*</span></span>

<span data-ttu-id="dd659-241">En la imagen siguiente se muestra el texto reconocido en la lista desplegable **resultado** .</span><span class="sxs-lookup"><span data-stu-id="dd659-241">The following image shows the recognized text in the **Result** drop-down list.</span></span>

<span data-ttu-id="dd659-242">![Aplicación dentro de awebpagewith reconocimiento de texto en la lista desplegable de resultados](images/demo-2.png)</span><span class="sxs-lookup"><span data-stu-id="dd659-242">![Application within awebpagewith recognized text in result drop-down list](images/demo-2.png)</span></span><br/>
<span data-ttu-id="dd659-243">*Aplicación dentro de awebpagewith reconocimiento de texto en la lista desplegable de resultados*</span><span class="sxs-lookup"><span data-stu-id="dd659-243">*Application within awebpagewith recognized text in result drop-down list*</span></span>

 

 



