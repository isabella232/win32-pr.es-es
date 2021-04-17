---
description: Las acciones personalizadas pueden agregar información de tiempo y progreso a un control ProgressBar. Para obtener más información sobre cómo crear un cuadro de diálogo para mostrar una acción con un control ProgressBar, vea crear un control ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Agregar acciones personalizadas a ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652627"
---
# <a name="adding-custom-actions-to-the-progressbar"></a><span data-ttu-id="25655-104">Agregar acciones personalizadas a ProgressBar</span><span class="sxs-lookup"><span data-stu-id="25655-104">Adding Custom Actions to the ProgressBar</span></span>

<span data-ttu-id="25655-105">[Las acciones personalizadas](custom-actions.md) pueden agregar información de tiempo y progreso a un control [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="25655-105">[Custom Actions](custom-actions.md) can add time and progress information to a [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="25655-106">Para obtener más información sobre cómo crear un cuadro de diálogo para mostrar una acción con un control ProgressBar, vea [crear un control ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="25655-106">For more information about creating an action display dialog box having a ProgressBar, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

<span data-ttu-id="25655-107">Tenga en cuenta que se deben agregar dos acciones personalizadas al paquete de Windows Installer para notificar con precisión la información de tiempo y progreso a ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="25655-107">Note that two custom actions must be added to the Windows Installer package to accurately report time and progress information to the ProgressBar.</span></span> <span data-ttu-id="25655-108">Una acción personalizada debe ser una acción personalizada diferida.</span><span class="sxs-lookup"><span data-stu-id="25655-108">One custom action must be a deferred custom action.</span></span> <span data-ttu-id="25655-109">Esta acción personalizada debe completar la instalación personalizada y enviar las cantidades de incrementos individuales al control [ProgressBar](progressbar-control.md) cuando el instalador ejecute el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="25655-109">This custom action should complete your custom installation and send the amounts of individual increments to the [ProgressBar](progressbar-control.md) control when the installer runs the installation script.</span></span> <span data-ttu-id="25655-110">La segunda acción personalizada debe ser una acción personalizada de ejecución inmediata que informe a la ProgressBar del número de pasos que se van a agregar al recuento total durante la fase de adquisición y generación de scripts de la instalación.</span><span class="sxs-lookup"><span data-stu-id="25655-110">The second custom action must be an immediate execution custom action that informs the ProgressBar how many ticks to add to the total count during the acquisition and script generation phase of the installation.</span></span>

<span data-ttu-id="25655-111">**Para agregar una acción personalizada a ProgressBar**</span><span class="sxs-lookup"><span data-stu-id="25655-111">**To add a custom action to the ProgressBar**</span></span>

1.  <span data-ttu-id="25655-112">Decida cómo la acción personalizada va a describir su progreso.</span><span class="sxs-lookup"><span data-stu-id="25655-112">Decide how the custom action will describe its progress.</span></span> <span data-ttu-id="25655-113">Por ejemplo, una acción personalizada que instala las claves del registro podría mostrar un mensaje de progreso y actualizar el [ProgressBar](progressbar-control.md) cada vez que el instalador escribe una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="25655-113">For example, a custom action that installs registry keys could display a progress message and update the [ProgressBar](progressbar-control.md) each time the installer writes one registry key.</span></span>
2.  <span data-ttu-id="25655-114">Cada actualización de la acción personalizada cambia la longitud de [ProgressBar](progressbar-control.md) mediante un incremento constante.</span><span class="sxs-lookup"><span data-stu-id="25655-114">Each update by the custom action changes the length of the [ProgressBar](progressbar-control.md) by a constant increment.</span></span> <span data-ttu-id="25655-115">Especifique o calcule el número de pasos en cada incremento.</span><span class="sxs-lookup"><span data-stu-id="25655-115">Specify or calculate the number of ticks in each increment.</span></span> <span data-ttu-id="25655-116">Normalmente, un cambio en la longitud de ProgressBar de un TIC corresponde a la instalación de un byte.</span><span class="sxs-lookup"><span data-stu-id="25655-116">Typically a change in ProgressBar length of one tick corresponds to the installation of one byte.</span></span> <span data-ttu-id="25655-117">Por ejemplo, si el instalador instala aproximadamente 10000 bytes cuando escribe una clave del registro, puede especificar que haya 10000 TICs en un incremento.</span><span class="sxs-lookup"><span data-stu-id="25655-117">For example, if the installer installs approximately 10000 bytes when it writes one registry key, you can specify that there are 10000 ticks in an increment.</span></span>
3.  <span data-ttu-id="25655-118">Especifique o calcule el número total de pasos que la acción personalizada agrega a la longitud de [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="25655-118">Specify or calculate the total number of ticks the custom action adds to the length of the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="25655-119">El número de pasos agregados por la acción personalizada se calcula normalmente como: (incremento de tick) x (número de elementos).</span><span class="sxs-lookup"><span data-stu-id="25655-119">The number of ticks added by the custom action is usually calculated as: (tick increment) x (number of items).</span></span> <span data-ttu-id="25655-120">Por ejemplo, si la acción personalizada escribe 10 claves del registro, el instalador instala aproximadamente 100000 bytes y, por tanto, el instalador debe aumentar la estimación de la longitud total final de ProgressBar en 100000 TICs.</span><span class="sxs-lookup"><span data-stu-id="25655-120">For example, if the custom action writes 10 registry keys, the installer installs approximately 100000 bytes and the installer therefore must increase the estimate of the final total length of the ProgressBar by 100000 ticks.</span></span>
    > [!Note]  
    > <span data-ttu-id="25655-121">Para calcular esto de forma dinámica, la acción personalizada debe contener una sección que se ejecute inmediatamente durante la generación del script.</span><span class="sxs-lookup"><span data-stu-id="25655-121">To calculate this dynamically, the custom action must contain a section that is immediately executed during script generation.</span></span> <span data-ttu-id="25655-122">La cantidad de TICs que notifique la acción personalizada de ejecución aplazada debe ser igual al número de pasos agregados al recuento de pasos total por la acción de ejecución inmediata.</span><span class="sxs-lookup"><span data-stu-id="25655-122">The amount of ticks reported by your deferred execution custom action must be equal to the number of ticks added to the total tick count by the immediate execution action.</span></span> <span data-ttu-id="25655-123">Si no es así, el tiempo restante tal y como lo notifica el control de texto TimeRemaining será incorrecto.</span><span class="sxs-lookup"><span data-stu-id="25655-123">If this is not the case, the time remaining as reported by the TimeRemaining text control will be inaccurate.</span></span>

     

4.  <span data-ttu-id="25655-124">Separe la acción personalizada en dos secciones de código: una sección que se ejecuta durante la fase de generación de scripts y una sección que se ejecuta durante la fase de ejecución de la instalación.</span><span class="sxs-lookup"><span data-stu-id="25655-124">Separate your custom action into two sections of code: a section that runs during the script generation phase and a section that runs during the execution phase of the installation.</span></span> <span data-ttu-id="25655-125">Puede hacerlo mediante dos archivos o puede usar un archivo acondicionado en el modo de ejecución del instalador.</span><span class="sxs-lookup"><span data-stu-id="25655-125">You can do this using two files or you can use one file by conditioning on the run mode of the installer.</span></span> <span data-ttu-id="25655-126">En el ejemplo siguiente se usa un archivo y se comprueba el estado de la instalación.</span><span class="sxs-lookup"><span data-stu-id="25655-126">The following sample uses one file and checks the installation state.</span></span> <span data-ttu-id="25655-127">Las secciones de la muestra están condicionadas a ejecutarse dependiendo de si el instalador está en la fase de ejecución o generación de scripts de la instalación.</span><span class="sxs-lookup"><span data-stu-id="25655-127">Sections of the sample are conditioned to run depending on whether the installer is in the execution or script generation phase of the installation.</span></span>
5.  <span data-ttu-id="25655-128">La sección que se ejecuta durante la generación de scripts debe aumentar la estimación de la longitud total final de [ProgressBar](progressbar-control.md) por el número total de TICs en la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="25655-128">The section that runs during script generation should increase the estimate of the final total length of the [ProgressBar](progressbar-control.md) by the total number of ticks in the custom action.</span></span> <span data-ttu-id="25655-129">Esto se hace mediante el envío de un mensaje de progreso de **ProgressAddition** .</span><span class="sxs-lookup"><span data-stu-id="25655-129">This is done by sending a **ProgressAddition** progress message.</span></span>
6.  <span data-ttu-id="25655-130">La sección que se ejecuta durante la fase de ejecución de la instalación debe configurar el texto y las plantillas del mensaje para informar al usuario sobre lo que está haciendo la acción personalizada y dirigir al instalador para que actualice el control [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="25655-130">The section that runs during the execution phase of installation should set up message text and templates to inform the user about what the custom action is doing and to direct the installer on updating the [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="25655-131">Por ejemplo, informe al instalador de que debe avanzar un incremento de la barra de progreso y enviar un mensaje de progreso explícito con cada actualización.</span><span class="sxs-lookup"><span data-stu-id="25655-131">For example, inform the installer to move the ProgressBar forward one increment and send an explicit progress message with each update.</span></span> <span data-ttu-id="25655-132">Normalmente, hay un bucle en esta sección si la acción personalizada está instalando algo.</span><span class="sxs-lookup"><span data-stu-id="25655-132">There is usually a loop in this section if the custom action is installing something.</span></span> <span data-ttu-id="25655-133">Con cada paso a través de este bucle, el instalador puede instalar un elemento de referencia, como una clave del registro y actualizar el control ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="25655-133">With each pass through this loop, the installer can install one reference item such as a registry key and update the ProgressBar control</span></span>
7.  <span data-ttu-id="25655-134">Agregue una acción personalizada de ejecución inmediata al paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="25655-134">Add an immediate execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="25655-135">Esta acción personalizada informa a [ProgressBar](progressbar-control.md) de cuánto debe avanzar durante la adquisición y las fases de generación de scripts de la instalación.</span><span class="sxs-lookup"><span data-stu-id="25655-135">This custom action informs the [ProgressBar](progressbar-control.md) how much to advance during the aquisition and script generation phases of the installation.</span></span> <span data-ttu-id="25655-136">En el ejemplo siguiente, el origen es el archivo DLL que se crea al compilar el código de ejemplo y el destino es el punto de entrada, CAProgress.</span><span class="sxs-lookup"><span data-stu-id="25655-136">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
8.  <span data-ttu-id="25655-137">Agregue una acción personalizada de ejecución aplazada al paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="25655-137">Add a deferred execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="25655-138">Esta acción personalizada completa los pasos de la instalación real e informa a la [ProgressBar](progressbar-control.md) de cuánto debe avanzar la barra en el momento en que el instalador ejecuta el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="25655-138">This custom action completes the steps of the actual installation and informs the [ProgressBar](progressbar-control.md) how much to advance the bar at the time when the installer runs the installation script.</span></span> <span data-ttu-id="25655-139">En el ejemplo siguiente, el origen es el archivo DLL que se crea al compilar el código de ejemplo y el destino es el punto de entrada, CAProgress.</span><span class="sxs-lookup"><span data-stu-id="25655-139">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
9.  <span data-ttu-id="25655-140">Programe ambas acciones personalizadas entre [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25655-140">Schedule both custom actions between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the [InstallExecuteSequence](installexecutesequence-table.md) table.</span></span> <span data-ttu-id="25655-141">La acción personalizada diferida debe programarse inmediatamente después de la acción personalizada de la ejecución inmediata.</span><span class="sxs-lookup"><span data-stu-id="25655-141">The deferred custom action should be scheduled immediately after the immediate execution custom action.</span></span> <span data-ttu-id="25655-142">El instalador no ejecutará la acción personalizada aplazada hasta que se ejecute el script.</span><span class="sxs-lookup"><span data-stu-id="25655-142">The installer will not run the deferred custom action until the script is executed.</span></span>

<span data-ttu-id="25655-143">En el ejemplo siguiente se muestra cómo se puede Agregar una acción personalizada a [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="25655-143">The following sample shows how a custom action can be added to the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="25655-144">El origen de ambas acciones personalizadas es el archivo DLL que se crea al compilar el código de ejemplo y el destino de ambas acciones personalizadas es el punto de entrada, CAProgress.</span><span class="sxs-lookup"><span data-stu-id="25655-144">The source of both custom actions is the DLL created by compiling the sample code and the target of both custom actions is the entry point, CAProgress.</span></span> <span data-ttu-id="25655-145">Este ejemplo no realiza ningún cambio real en el sistema, sino que funciona como si se instalaran 10 elementos de referencia con un tamaño aproximado de 10.000 bytes.</span><span class="sxs-lookup"><span data-stu-id="25655-145">This sample does not make any actual changes to the system, but operates the ProgressBar as if installing 10 reference items that are each approximately 10,000 bytes in size.</span></span> <span data-ttu-id="25655-146">El instalador actualiza el mensaje y ProgressBar cada vez que instala un elemento de referencia.</span><span class="sxs-lookup"><span data-stu-id="25655-146">The installer updates the message and ProgressBar each time it installs a reference item.</span></span>


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



