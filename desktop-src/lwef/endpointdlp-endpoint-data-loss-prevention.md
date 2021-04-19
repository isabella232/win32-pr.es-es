---
description: Las API de prevención de pérdida de datos (DLP) del punto de conexión permiten a las aplicaciones notificar al sistema operativo antes y después de ciertas operaciones, como abrir o guardar un archivo.
title: Prevención de pérdida de datos de punto de conexión
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 867e059e0accfc1208c96394c3065d69cf9f576c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495831"
---
# <a name="endpoint-data-loss-prevention"></a>Prevención de pérdida de datos de punto de conexión

Windows 10 implementa mecanismos que ayudan a evitar la pérdida de datos de archivos confidenciales. Las API de prevención de pérdida de datos (DLP) del punto de conexión permiten a las aplicaciones notificar al sistema operativo antes y después de ciertas operaciones, como abrir o guardar un archivo. Estas notificaciones sirven como "sugerencias" que permiten al sistema optimizar las operaciones de pérdida de datos.

## <a name="location-of-the-dlp-dll"></a>Ubicación del archivo DLL dlp

Puesto que el archivo DLL DLP del punto de conexión no está incluido con el Windows SDK, las aplicaciones detendrán que cargar el archivo DLL manualmente en tiempo de ejecución. La ruta de acceso a la ubicación del archivo DLL se almacena en el Registro. En la tabla siguiente se enumeran las claves y los valores del Registro que almacenan esta información. Estas rutas de acceso se definen como constantes en la lista de código endpointdlp.h de ejemplo que se proporciona a continuación para mayor comodidad para los desarrolladores.

| Constante | Value | Descripción   |
|----------|-------|---------------|
| ENDPOINTDLP_DLL_NAME | "EndpointDlp.dll" | El nombre del archivo DLL dlp de punto de conexión que proporciona la API. |
| ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY | "SOFTWARE \\ Microsoft \\ Windows Defender" | Windows Defender clave del Registro en HKLM donde se almacenan algunos valores de DLP de punto de conexión |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY | Valor de ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |  La ruta de acceso del Registro bajo la clave HKLM desde la que EndpointDlp.dll la ubicación de instalación |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE | "InstallLocation" | Valor del Registro en ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY donde se almacena la EndpointDlp.dll de instalación |
| ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX | "x86" | En plataformas x64, concatene este directorio para obtener la versión x86 de EndpointDlp.dll |

## <a name="check-if-endpoint-dlp-is-enabled"></a>Comprobación de si el punto de conexión DLP está habilitado

Para determinar si dlp del punto de conexión está habilitado en el sistema, compruebe el siguiente valor de clave del Registro. 

| Constante | Value | Descripción   |
|----------|-------|---------------|
| ENDPOINTDLP_ENABLED_FLAG_REGKEY |  " \\ Características" | Ruta de acceso a la clave de marca habilitada para DLP de punto de conexión en (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |
| ENDPOINTDLP_ENABLED_FLAG_REGVALUE | "SenseDlpEnabled" | Valor del Registro en ENDPOINTDLP_ENABLED_FLAG_REGKEY que contiene la clave del Registro de marca habilitada para DLP

## <a name="endpoint-dlp-apis"></a>API DLP de punto de conexión

En las tablas siguientes se muestran las API proporcionadas por el archivo DLL DLP del punto de conexión.

### <a name="initialization-and-versioning"></a>Inicialización y control de versiones

| API | Descripción |
|-----|-------------|
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Notifica al sistema los modos de cumplimiento deseados para un conjunto de operaciones de prevención de pérdida de datos (DLP) de punto de conexión.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Recupera la versión de la API de prevención de pérdida de datos (DLP) del punto de conexión en el dispositivo actual.                                  |


### <a name="document-operations"></a>Operaciones de documento

| API | Descripción |
|-----|-------------|
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md) | Proporciona al sistema información sobre un documento antes de iniciar la operación de apertura. |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md) | Proporciona al sistema información sobre un documento una vez completada la operación de apertura.  |
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.                                  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Proporciona al sistema información sobre un documento antes de iniciar la operación de apertura.  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Proporciona al sistema información sobre un documento una vez completada la operación de apertura.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.                                  |

### <a name="save-as-operations"></a>Guardar como operaciones
| API | Descripción |
|-----|-------------|
| [DlpNotifyPreSaveAsDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Proporciona al sistema información sobre un documento antes de iniciar una operación de guardar como.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Proporciona al sistema información sobre un documento una vez completada la operación guardar como.                                  |


### <a name="drag-and-drop-operations"></a>Operaciones de arrastrar y colocar

| API | Descripción |
|-----|-------------|
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Proporciona al sistema información sobre un documento cuando se introduce un destino de colocación.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Proporciona al sistema información sobre un documento cuando se sale de un destino de colocación.                                  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de arrastrar y colocar.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Proporciona al sistema información sobre un documento una vez completada una operación de arrastrar y colocar.  |


### <a name="clipboard-operations"></a>opciones de Portapapeles

| API | Descripción |
|-----|-------------|
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de copia en el Portapapeles.  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Proporciona al sistema información sobre un documento una vez completada una operación de copia en el Portapapeles.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de pegar desde el Portapapeles.  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Proporciona al sistema información sobre un documento después de que se haya completado una operación de pegado del Portapapeles.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Proporciona al sistema información de estado una vez completada una operación de almacenamiento escalonado del Portapapeles.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifica al sistema antes de que se inicie una operación de almacenamiento escalonado del Portapapeles.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomar los datos de su caché interna.                                  |

### <a name="print-operations"></a>Operaciones de impresión

| API | Descripción |
|-----|-------------|
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de impresión.  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Proporciona al sistema información sobre un documento después de que se haya iniciado una operación de impresión.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Proporciona al sistema información sobre un documento una vez completada una operación de impresión.                                  |

## <a name="endpoint-dlp-example-header"></a>Encabezado de ejemplo dlp de punto de conexión

Dado que el encabezado DLP del punto de conexión no se incluye en el Windows SDK, debe crear el archivo de encabezado usted mismo para obtener firmas de API que se usarán en la implementación. Para su comodidad, proporcionamos código de ejemplo que puede copiar y pegar en la aplicación. Además de las declaraciones de función, esta lista de código también define constantes útiles, como la información de control de versiones y las rutas de acceso de clave del Registro.

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


```


