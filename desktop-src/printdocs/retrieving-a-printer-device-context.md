---
description: En este tema se describe cómo recuperar un contexto de dispositivo de impresora.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: 'Cómo: recuperar un contexto de dispositivo de impresora'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697390"
---
# <a name="how-to-retrieve-a-printer-device-context"></a>Cómo: recuperar un contexto de dispositivo de impresora

En este tema se describe cómo recuperar un contexto de dispositivo de impresora. Puede recuperar un contexto de dispositivo de impresora llamando directamente a la función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o puede ser devuelto por un cuadro de diálogo de **impresión** común.

Cuando se muestra un cuadro de diálogo **Imprimir** común, el usuario podrá seleccionar la impresora, las páginas del documento y el número de copias del documento que desee imprimir. El cuadro de diálogo **Imprimir** común devuelve estas selecciones en una estructura de datos.

En este tema se describe cómo obtener un contexto de dispositivo de impresora mediante los métodos siguientes.

-   [Llamar a CreateDC](#call-createdc)
-   [Mostrar un cuadro de diálogo de impresión común](#display-a-print-common-dialog-box)
    -   [Usar la función PrintDlgEx](#using-the-printdlgex-function)
    -   [Usar la función PrintDlg](#using-the-printdlg-function)

## <a name="call-createdc"></a>Llamar a CreateDC

Si conoce el dispositivo en el que desea imprimir, puede llamar a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) y pasar esa información directamente a la función. **CreateDC** devuelve un contexto de dispositivo en el que se puede representar el contenido que se va a imprimir.

La llamada más sencilla para recuperar un contexto de dispositivo se muestra en el ejemplo de código siguiente. El código de este ejemplo recupera un contexto de dispositivo en el dispositivo de pantalla predeterminado.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Para representar en una impresora específica, debe especificar "WINSPOOL" como el dispositivo y pasar el nombre correcto de la impresora a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). También puede pasar una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en la llamada a **CreateDC** si desea proporcionar datos de inicialización específicos del dispositivo para el controlador del dispositivo al crear el contexto del dispositivo.

En el ejemplo siguiente se muestra una llamada a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) en la que se selecciona el controlador "WINSPOOL" y el nombre de la impresora se especifica mediante el nombre.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



Puede obtener la cadena de nombre de impresora exacta que se va a pasar a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) mediante una llamada a la función [**EnumPrinters**](enumprinters.md) . En el ejemplo de código siguiente se muestra cómo llamar a **EnumPrinters** y obtener los nombres de las impresoras locales y conectadas localmente. Dado que el tamaño del búfer necesario no se puede conocer de antemano, se llama dos veces a **EnumPrinters** . La primera llamada devuelve el tamaño del búfer necesario. Esa información se utiliza para asignar un búfer del tamaño requerido y la segunda llamada a **EnumPrinters** devuelve los datos que desea.


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a>Mostrar un cuadro de diálogo de impresión común

Puede elegir entre dos cuadros de diálogo de **impresión** comunes para mostrar a un usuario; el cuadro de diálogo más reciente, que se puede mostrar mediante una llamada a la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) y el cuadro de diálogo estilo anterior, que se puede mostrar mediante una llamada a la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . En las secciones siguientes se describe cómo llamar a cada cuadro de diálogo desde una aplicación.

### <a name="using-the-printdlgex-function"></a>Usar la función PrintDlgEx

Llame a la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para mostrar la hoja de propiedades **Print** . Mediante el uso de la hoja de propiedades, el usuario puede especificar información sobre el trabajo de impresión. Por ejemplo, el usuario puede seleccionar un intervalo de páginas para imprimir, el número de copias, etc. El **PrintDlgEx** también puede recuperar un identificador de un contexto de dispositivo para la impresora seleccionada. Puede utilizar el identificador para representar la salida en la impresora.

Para ver el código de ejemplo que muestra el uso de [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para recuperar un contexto de dispositivo de impresora, vea el tema sobre cómo usar la hoja de propiedades de impresión en [uso de cuadros de diálogo comunes](../dlgbox/using-common-dialog-boxes.md).

### <a name="using-the-printdlg-function"></a>Usar la función PrintDlg

Si la aplicación se debe ejecutar en un sistema que no admite la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , como en un sistema que ejecuta una versión de Windows anterior a Windows 2000, o no necesita la funcionalidad adicional que proporciona la función **PrintDlgEx** , use la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . En los pasos siguientes se describe cómo mostrar el cuadro de diálogo común **Imprimir** estilo anterior.

1.  Inicialice la estructura de datos [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Llame a [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para mostrar el cuadro de diálogo **Imprimir** común al usuario.
3.  Si la llamada a [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve **true**, bloquee la memoria de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelta. Si la llamada **PrintDlg** devuelve **false**, el usuario presionó el botón **Cancelar** en el cuadro de diálogo **Imprimir** común, por lo que no hay nada más que procesar.
4.  Asigne un búfer de memoria local que sea lo suficientemente grande como para contener una copia de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .
5.  Copie la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelta a la asignada localmente.
6.  Guarde la información que se devuelve en la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y que tendrá que procesar el trabajo de impresión.
7.  Libere el [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y los búferes de memoria a los que hace referencia.

En el ejemplo de código siguiente se muestra cómo usar la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para obtener el contexto de dispositivo y el nombre de la impresora seleccionada.


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



Para obtener más información acerca de la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , vea "Mostrar el cuadro de diálogo Imprimir" en el tema sobre el [uso de cuadros de diálogo comunes](../dlgbox/using-common-dialog-boxes.md).

 

 
