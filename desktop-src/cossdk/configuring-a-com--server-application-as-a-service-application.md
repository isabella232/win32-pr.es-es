---
description: Se puede crear una aplicación de servidor COM+ como servicio para que se inicie automáticamente durante el inicio del sistema o manualmente mediante las activaciones.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configuración de una aplicación de servidor COM+ como aplicación de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907092"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a><span data-ttu-id="d8006-103">Configuración de una aplicación de servidor COM+ como aplicación de servicio</span><span class="sxs-lookup"><span data-stu-id="d8006-103">Configuring a COM+ Server Application as a Service Application</span></span>

<span data-ttu-id="d8006-104">Se puede crear una aplicación de servidor COM+ como servicio para que se inicie automáticamente durante el inicio del sistema o manualmente mediante las activaciones.</span><span class="sxs-lookup"><span data-stu-id="d8006-104">A COM+ server application can be created as a service to start either automatically during the system startup or manually by activations.</span></span> <span data-ttu-id="d8006-105">Si el servicio no se inicia, la opción para el control de errores especifica la gravedad del error y determina la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="d8006-105">If the service fails to start, the option for error handling specifies the severity of the error and determines the action to be taken.</span></span> <span data-ttu-id="d8006-106">También está disponible la opción para configurar un servicio para que se ejecute como la cuenta de sistema local, así como la opción para asignar una cuenta de usuario específica para la que se ejecutará la aplicación de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="d8006-106">The option to configure a service to run as the local system account is also available, as well as the option to assign a specific user account for which the COM+ server application will run.</span></span> <span data-ttu-id="d8006-107">Las dependencias también se pueden seleccionar en una lista de servicios registrados en el equipo con servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="d8006-107">Dependencies can also be selected from a list of services registered on the computer using Component Services.</span></span> <span data-ttu-id="d8006-108">Esto determinará qué servicios deben ejecutarse antes de que se inicie este servicio.</span><span class="sxs-lookup"><span data-stu-id="d8006-108">This will determine which services must be executed before this service is started.</span></span>

<span data-ttu-id="d8006-109">**Para configurar una aplicación COM+ para que se ejecute como un servicio**</span><span class="sxs-lookup"><span data-stu-id="d8006-109">**To configure a COM+ application to run as a service**</span></span>

1.  <span data-ttu-id="d8006-110">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación de servidor COM+ que desea ejecutar como servicio.</span><span class="sxs-lookup"><span data-stu-id="d8006-110">In the console tree of the Component Services administrative tool, locate the COM+ server application you want to run as a service.</span></span>

2.  <span data-ttu-id="d8006-111">Haga clic con el botón secundario en la aplicación de servidor COM+ y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="d8006-111">Right-click the COM+ server application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="d8006-112">En el cuadro de diálogo **propiedades** , haga clic en la pestaña **activación** .</span><span class="sxs-lookup"><span data-stu-id="d8006-112">In the **Properties** dialog box, click the **Activation** tab.</span></span>

4.  <span data-ttu-id="d8006-113">En el cuadro **tipo de activación** , active la casilla **Ejecutar aplicación como servicio NT** .</span><span class="sxs-lookup"><span data-stu-id="d8006-113">In the **Activation type** box, check the **Run application as NT Service** check box.</span></span>

    > [!Note]  
    > <span data-ttu-id="d8006-114">La casilla **Ejecutar aplicación como servicio NT** solo está habilitada para aplicaciones de servidor y está deshabilitada para las aplicaciones de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d8006-114">The **Run application as NT Service** check box is enabled only for server applications and is disabled for library applications.</span></span>

     

5.  <span data-ttu-id="d8006-115">Haga clic en el botón **instalar nuevo servicio** .</span><span class="sxs-lookup"><span data-stu-id="d8006-115">Click the **Setup New Service** button.</span></span>

6.  <span data-ttu-id="d8006-116">En el cuadro **tipo de inicio** del cuadro de diálogo nombre de **servicio** , seleccione **automático** o **manual**.</span><span class="sxs-lookup"><span data-stu-id="d8006-116">In the **Startup type** box in the **Service Name** dialog box, select **Automatic** or **Manual**.</span></span>

7.  <span data-ttu-id="d8006-117">Opta Para especificar la acción que se va a realizar para un error determinado, seleccione **omitir**, **normal**, **grave** o **crítico** en el cuadro **tratamiento de errores** .</span><span class="sxs-lookup"><span data-stu-id="d8006-117">(Optional) To specify the action to be taken for a particular error, select **Ignore**, **Normal**, **Severe**, or **Critical** in the **Error Handling** box.</span></span> <span data-ttu-id="d8006-118">El comportamiento asociado a cada opción es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8006-118">The behavior associated with each option is as follows:</span></span>

    1.  <span data-ttu-id="d8006-119">**Ignore**.</span><span class="sxs-lookup"><span data-stu-id="d8006-119">**Ignore**.</span></span> <span data-ttu-id="d8006-120">El programa de inicio registra el error, pero continúa con la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="d8006-120">The startup program logs the error but continues the startup operation.</span></span>
    2.  <span data-ttu-id="d8006-121">**Normal**.</span><span class="sxs-lookup"><span data-stu-id="d8006-121">**Normal**.</span></span> <span data-ttu-id="d8006-122">El error se registra, se muestra un cuadro de mensaje y el programa de inicio continúa con la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="d8006-122">The error is logged, a message box is displayed, and the startup program continues the startup operation.</span></span>
    3.  <span data-ttu-id="d8006-123">**Grave**.</span><span class="sxs-lookup"><span data-stu-id="d8006-123">**Severe**.</span></span> <span data-ttu-id="d8006-124">El error se registra y el sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="d8006-124">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="d8006-125">Si se trata de la última configuración válida conocida que se está iniciando cuando se registra el error, la operación de inicio continúa.</span><span class="sxs-lookup"><span data-stu-id="d8006-125">If it is the last known good configuration that is being started when the error is logged, the startup operation continues.</span></span>
    4.  <span data-ttu-id="d8006-126">**Critica**.</span><span class="sxs-lookup"><span data-stu-id="d8006-126">**Critical**.</span></span> <span data-ttu-id="d8006-127">El error se registra y el sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="d8006-127">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="d8006-128">Si se trata de la última configuración válida conocida que se está iniciando cuando se registra el error, se produce un error en la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="d8006-128">If it is the last known good configuration that is being started when the error is logged, the startup operation fails.</span></span>

8.  <span data-ttu-id="d8006-129">Opta Para establecer otros servicios como dependientes, seleccione los servicios dependientes en la lista del cuadro **dependencias** .</span><span class="sxs-lookup"><span data-stu-id="d8006-129">(Optional) To set other services as dependent, select the dependent services from the list in the **Dependencies** box.</span></span>

9.  <span data-ttu-id="d8006-130">Opta Para indicar que se debe permitir que el servicio interactúe con el escritorio, active la casilla permitir que el **servicio interactúe con el escritorio** .</span><span class="sxs-lookup"><span data-stu-id="d8006-130">(Optional) To indicate that the service should be allowed to interact with the desktop, check the **Allow service to interact with desktop** check box.</span></span>

10. <span data-ttu-id="d8006-131">Haga clic en **Crear**.</span><span class="sxs-lookup"><span data-stu-id="d8006-131">Click **Create**.</span></span>

11. <span data-ttu-id="d8006-132">Opta Para asignar el servicio a una cuenta de usuario:</span><span class="sxs-lookup"><span data-stu-id="d8006-132">(Optional) To assign the service to a user account:</span></span>

    1.  <span data-ttu-id="d8006-133">En la pestaña **identidad** , seleccione **este usuario**.</span><span class="sxs-lookup"><span data-stu-id="d8006-133">In the **Identity** tab, select **This user**.</span></span>
    2.  <span data-ttu-id="d8006-134">Para seleccionar el usuario, escriba el nombre de usuario en el cuadro **usuario** o haga clic en el botón **examinar** .</span><span class="sxs-lookup"><span data-stu-id="d8006-134">To select the user, enter the user name in the **User** box or click the **Browse** button.</span></span>
    3.  <span data-ttu-id="d8006-135">Escriba la contraseña de la cuenta de usuario en el cuadro **contraseña** .</span><span class="sxs-lookup"><span data-stu-id="d8006-135">Enter the password for the user account in the **Password** box.</span></span>
    4.  <span data-ttu-id="d8006-136">Escriba la misma contraseña en el cuadro **Confirmar contraseña** .</span><span class="sxs-lookup"><span data-stu-id="d8006-136">Enter the same password in the **Confirm Password** box.</span></span>

 

 



