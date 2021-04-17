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
# <a name="adding-custom-actions-to-the-progressbar"></a>Agregar acciones personalizadas a ProgressBar

[Las acciones personalizadas](custom-actions.md) pueden agregar información de tiempo y progreso a un control [ProgressBar](progressbar-control.md) . Para obtener más información sobre cómo crear un cuadro de diálogo para mostrar una acción con un control ProgressBar, vea [crear un control ProgressBar](authoring-a-progressbar-control.md).

Tenga en cuenta que se deben agregar dos acciones personalizadas al paquete de Windows Installer para notificar con precisión la información de tiempo y progreso a ProgressBar. Una acción personalizada debe ser una acción personalizada diferida. Esta acción personalizada debe completar la instalación personalizada y enviar las cantidades de incrementos individuales al control [ProgressBar](progressbar-control.md) cuando el instalador ejecute el script de instalación. La segunda acción personalizada debe ser una acción personalizada de ejecución inmediata que informe a la ProgressBar del número de pasos que se van a agregar al recuento total durante la fase de adquisición y generación de scripts de la instalación.

**Para agregar una acción personalizada a ProgressBar**

1.  Decida cómo la acción personalizada va a describir su progreso. Por ejemplo, una acción personalizada que instala las claves del registro podría mostrar un mensaje de progreso y actualizar el [ProgressBar](progressbar-control.md) cada vez que el instalador escribe una clave del registro.
2.  Cada actualización de la acción personalizada cambia la longitud de [ProgressBar](progressbar-control.md) mediante un incremento constante. Especifique o calcule el número de pasos en cada incremento. Normalmente, un cambio en la longitud de ProgressBar de un TIC corresponde a la instalación de un byte. Por ejemplo, si el instalador instala aproximadamente 10000 bytes cuando escribe una clave del registro, puede especificar que haya 10000 TICs en un incremento.
3.  Especifique o calcule el número total de pasos que la acción personalizada agrega a la longitud de [ProgressBar](progressbar-control.md). El número de pasos agregados por la acción personalizada se calcula normalmente como: (incremento de tick) x (número de elementos). Por ejemplo, si la acción personalizada escribe 10 claves del registro, el instalador instala aproximadamente 100000 bytes y, por tanto, el instalador debe aumentar la estimación de la longitud total final de ProgressBar en 100000 TICs.
    > [!Note]  
    > Para calcular esto de forma dinámica, la acción personalizada debe contener una sección que se ejecute inmediatamente durante la generación del script. La cantidad de TICs que notifique la acción personalizada de ejecución aplazada debe ser igual al número de pasos agregados al recuento de pasos total por la acción de ejecución inmediata. Si no es así, el tiempo restante tal y como lo notifica el control de texto TimeRemaining será incorrecto.

     

4.  Separe la acción personalizada en dos secciones de código: una sección que se ejecuta durante la fase de generación de scripts y una sección que se ejecuta durante la fase de ejecución de la instalación. Puede hacerlo mediante dos archivos o puede usar un archivo acondicionado en el modo de ejecución del instalador. En el ejemplo siguiente se usa un archivo y se comprueba el estado de la instalación. Las secciones de la muestra están condicionadas a ejecutarse dependiendo de si el instalador está en la fase de ejecución o generación de scripts de la instalación.
5.  La sección que se ejecuta durante la generación de scripts debe aumentar la estimación de la longitud total final de [ProgressBar](progressbar-control.md) por el número total de TICs en la acción personalizada. Esto se hace mediante el envío de un mensaje de progreso de **ProgressAddition** .
6.  La sección que se ejecuta durante la fase de ejecución de la instalación debe configurar el texto y las plantillas del mensaje para informar al usuario sobre lo que está haciendo la acción personalizada y dirigir al instalador para que actualice el control [ProgressBar](progressbar-control.md) . Por ejemplo, informe al instalador de que debe avanzar un incremento de la barra de progreso y enviar un mensaje de progreso explícito con cada actualización. Normalmente, hay un bucle en esta sección si la acción personalizada está instalando algo. Con cada paso a través de este bucle, el instalador puede instalar un elemento de referencia, como una clave del registro y actualizar el control ProgressBar.
7.  Agregue una acción personalizada de ejecución inmediata al paquete de Windows Installer. Esta acción personalizada informa a [ProgressBar](progressbar-control.md) de cuánto debe avanzar durante la adquisición y las fases de generación de scripts de la instalación. En el ejemplo siguiente, el origen es el archivo DLL que se crea al compilar el código de ejemplo y el destino es el punto de entrada, CAProgress.
8.  Agregue una acción personalizada de ejecución aplazada al paquete de Windows Installer. Esta acción personalizada completa los pasos de la instalación real e informa a la [ProgressBar](progressbar-control.md) de cuánto debe avanzar la barra en el momento en que el instalador ejecuta el script de instalación. En el ejemplo siguiente, el origen es el archivo DLL que se crea al compilar el código de ejemplo y el destino es el punto de entrada, CAProgress.
9.  Programe ambas acciones personalizadas entre [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) . La acción personalizada diferida debe programarse inmediatamente después de la acción personalizada de la ejecución inmediata. El instalador no ejecutará la acción personalizada aplazada hasta que se ejecute el script.

En el ejemplo siguiente se muestra cómo se puede Agregar una acción personalizada a [ProgressBar](progressbar-control.md). El origen de ambas acciones personalizadas es el archivo DLL que se crea al compilar el código de ejemplo y el destino de ambas acciones personalizadas es el punto de entrada, CAProgress. Este ejemplo no realiza ningún cambio real en el sistema, sino que funciona como si se instalaran 10 elementos de referencia con un tamaño aproximado de 10.000 bytes. El instalador actualiza el mensaje y ProgressBar cada vez que instala un elemento de referencia.


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



 

 



