---
description: Referencia para las funciones de C++ Windows Runtime.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: Funciones (Windows Runtime)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: 1ed2ea39385ac5cb7afc34770a5ee2d2a572bb8b
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105700440"
---
# <a name="functions-windows-runtime-c-reference"></a>Funciones (referencia de Windows Runtime C++)

## <a name="in-this-section"></a>En esta sección



| Función | Descripción |
|-|-|
| [**CoDecodeProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Busca la implementación de una interfaz del modelo de objetos componentes (COM) en un proceso de servidor a partir de una interfaz para un objeto de proxy. |
| [**CreateControlInput**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Crea un objeto [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) en el subproceso de la interfaz de usuario del llamador. |
| [**CreateControlInputEx**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Crea un objeto [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) en un subproceso de trabajo o en el subproceso de la interfaz de usuario.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Crea una instancia de IDirect3DDevice a partir de un IDXGIDevice. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Crea una instancia de IDirect3DSurface a partir de un IDXGISurface. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Crea una instancia de [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) a partir de un [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice). |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Crea una instancia de [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) a partir de un [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface). |
| [**CreateRandomAccessStreamOnFile**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | Crea una secuencia de acceso aleatorio Windows Runtime para un archivo. |
| [**CreateRandomAccessStreamOverStream**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | Crea una secuencia de acceso aleatorio Windows Runtime en torno a una implementación base de [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . |
| [**CreateStreamOverRandomAccessStream**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | Crea una [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) en torno a un objeto Windows Runtime [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) . |
| [**CreateXamlUIPresenter**](createxamluipresenter.md) | Una función de creador estático que puede crear un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) para una superficie de representación en una aplicación de escritorio. |
| [**DbgRaiseAssertionFailure**](/previous-versions//jj635749(v=vs.85)) | Genera una aserción para la depuración.  |
| [**GetDXGIInterface (IDirect3DDevice ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Recupera una interfaz de DXGI de una instancia de [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) . |
| [**GetDXGIInterface (IDirect3DSurface ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Recupera una interfaz de DXGI de una instancia de [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) . |
| [**GetDXGIInterfaceFromObject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Recupera una interfaz de DXGI de un objeto. |
| [**GetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Obtiene el objeto de información de error restringido establecido por una llamada anterior a [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) en el subproceso lógico actual. |
| [**HSTRING \_ UserFree**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Libera los recursos en el lado del servidor cuando los llama los archivos de código auxiliar de RPC. |
| [**HSTRING \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Libera los recursos en el lado del servidor cuando los llama los archivos de código auxiliar de RPC.  |
| [**HSTRING \_ UserMarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Calcula las referencias de un objeto [**HSTRING**](hstring.md) en el búfer de RPC. |
| [**HSTRING \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Calcula las referencias de un objeto [**HSTRING**](hstring.md) en el búfer de RPC. |
| [**Usuarios de HSTRING \_**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Calcula el tamaño del hilo del objeto [**HSTRING**](hstring.md) y obtiene su identificador y sus datos. |
| [**HSTRING \_ UserSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Calcula el tamaño del hilo del objeto [**HSTRING**](hstring.md) y obtiene su identificador y sus datos. |
| [**HSTRING \_ UserUnmarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Quita las referencias de un objeto [**HSTRING**](hstring.md) del búfer de RPC. |
| [**HSTRING \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Quita las referencias de un objeto [**HSTRING**](hstring.md) del búfer de RPC. |
| [**IsErrorPropagationEnabled**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | Indica si el evento [**CoreApplication. UnhandledErrorDetected**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) se produce para los errores devueltos por el delegado registrado como una función de devolución de llamada para un evento Windows Runtime API o la finalización de un método asincrónico. |
| [**DllGetActivationFactory**](/previous-versions//br205771(v=vs.85)) | Recupera el generador de activación de un archivo DLL que contiene clases que se van a activar Windows Runtime. |
| [**MetaDataGetDispenser**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Crea una clase de dispensador. |
| [**PdfCreateRenderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Obtiene una instancia de la interfaz [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) para mostrar una sola página de un archivo Portable Document Format (pdf). |
| [**PdfRenderParams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Rellena un estructura [**de \_ \_ parámetros de representación en PDF**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) . Una \_ estructura de parámetros de representación en PDF \_ representa un conjunto de propiedades para la generación de una única página de un archivo PDF. |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | Activa la clase de Windows Runtime especificada. |
| [**RoCaptureErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Guarda el contexto de error actual para que esté disponible para las llamadas posteriores a la función [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) . |
| [**RoClearError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Quita la información de error existente del bloque de entorno del subproceso actual (TEB). |
| [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Genera una excepción no continuable en el proceso actual. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Genera una excepción no continuada en el proceso actual y también permite incluir el contexto de error adicional aún no capturado por el sistema operativo. |
| [**RoFreeParameterizedTypeExtra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Libera el identificador asignado por [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid). |
| [**RoGetActivatableClassRegistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Habilita la recuperación de la información de registro de la clase. |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Obtiene el generador de activación para la clase en tiempo de ejecución especificada. |
| [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Crea una referencia ágil para un objeto especificado por la interfaz especificada. |
| [**RoGetApartmentIdentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Obtiene un identificador único para el apartamento actual. |
| [**RoGetBufferMarshaler**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Proporciona un contador de referencias de IBuffer estándar para implementar la semántica asociada a la interfaz IBuffer cuando se calculan las referencias. |
| [**RoGetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | Obtiene el comportamiento actual de informes de Windows Runtime funciones de error. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Busca y recupera el archivo de metadatos que describe la interfaz binaria de aplicación (ABI) del TypeName especificado. |
| [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Calcula el identificador de interfaz (IID) de la interfaz o el tipo de delegado que se produce cuando se crea una instancia de un delegado o una interfaz con parámetros con los argumentos de tipo especificados. |
| [**RoGetServerActivatableClasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Recupera las clases activables que están registradas para un servidor ejecutable determinado (EXE), que se registró en el identificador de paquete del proceso de llamada. |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | Inicializa el Windows Runtime en el subproceso actual con el modelo de simultaneidad especificado. |
| [**RoInspectThreadErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Obtiene el objeto de error que representa la pila de llamadas en el punto en el que se originó el error. |
| [**RoInspectCapturedStackBackTrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Proporciona una manera de que los depuradores inspeccionen una pila de llamadas desde un proceso de destino. |
| [**RoOriginateError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Notifica un error y una cadena informativa a un depurador asociado. |
| [**RoOriginateErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Notifica un error y una cadena informativa a un depurador asociado. |
| [**RoOriginateLanguageException**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Notifica un error, una cadena informativa y un objeto de error a un depurador asociado. |
| [**RoParameterizedTypeExtraGetTypeSignature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Obtiene la firma de tipo utilizada para calcular el IID de la última llamada a [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) con el identificador especificado. |
| [**RoParseTypeName**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Analiza un nombre de tipo y los parámetros de tipo existentes, en el caso de tipos parametrizados. |
| [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | Registra los generadores de activación fuera de proceso de una matriz para un servidor Windows Runtime exe. |
| [**RoRegisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Registra una devolución de llamada de [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) que se invocará cuando se cierre el apartamento actual. |
| [**RoReportUnhandledError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Desencadena el controlador de errores global cuando se produce una excepción no controlada. |
| [**RoReportFailedDelegate**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Desencadena el controlador de errores global cuando se produce un error de delegado. |
| [**RoResolveNamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | Determine los elementos secundarios directos, los tipos y los subespacios de nombres del espacio de nombres de Windows Runtime especificado, de cualquier lenguaje de programación admitido por el Windows Runtime. |
| [**RoResolveRestrictedErrorInfoReference**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Devuelve el puntero de la interfaz [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) basándose en la referencia especificada. |
| [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | Quita una matriz de generadores de activación registrados del Windows Runtime. |
| [**RoSetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | Establece el comportamiento de los informes de Windows Runtime funciones de error. |
| [**RoTransformError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Notifica un error modificado y una cadena informativa a un depurador asociado. |
| [**RoTransformErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Notifica un error transformado y una cadena informativa a un depurador asociado. |
| [**RoUninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | Cierra el Windows Runtime en el subproceso actual. |
| [**RoUnregisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Anula el registro de una interfaz [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) registrada previamente. |
| [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Establece el objeto de información de error restringido para el subproceso actual. |
| [**WindowsCompareStringOrdinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Compara dos objetos [**HSTRING**](hstring.md) especificados y devuelve un entero que indica su posición relativa en un criterio de ordenación. |
| [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Concatena dos cadenas especificadas. |
| [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Crea un nuevo [**HSTRING**](hstring.md) basándose en la cadena de origen especificada. |
| [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Crea una nueva referencia de cadena basada en la cadena especificada. |
| [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Disminuye el recuento de referencias de un búfer de cadena. |
| [**WindowsDeleteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Descarta un búfer de cadena preasignado si no se promovió a un [**HSTRING**](hstring.md). |
| [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Crea una copia de la cadena especificada. |
| [**WindowsGetStringLen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Obtiene la longitud, en caracteres Unicode, de la cadena especificada. |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Obtiene el búfer de respaldo de la cadena especificada. |
| [**WindowsInspectString**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | Proporciona una manera para que los depuradores muestren el valor de un Windows Runtime [**HSTRING**](hstring.md) en otro espacio de direcciones, de forma remota o desde un volcado de memoria.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | Proporciona una manera para que los depuradores muestren el valor de un Windows Runtime [**HSTRING**](hstring.md) en otro espacio de direcciones, de forma remota o desde un volcado de memoria.  |
| [**WindowsIsStringEmpty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Indica si la cadena especificada es una cadena vacía. |
| [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Asigna un búfer de caracteres mutable para su uso en la creación de [**HSTRING**](hstring.md) . |
| [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Crea un [**HSTRING**](hstring.md) a partir del [**\_ búfer HSTRING**](hstring-buffer.md)especificado. |
| [**WindowsReplaceString**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Reemplaza todas las apariciones de un conjunto de caracteres en la cadena especificada por otro conjunto de caracteres para crear una nueva cadena. |
| [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Indica si la cadena especificada tiene caracteres nulos incrustados. |
| [**WindowsSubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Recupera una subcadena de la cadena especificada. La subcadena comienza en la posición del carácter que se haya especificado. |
| [**WindowsSubstringWithSpecifiedLength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Recupera una subcadena de la cadena especificada. La subcadena comienza en una posición de carácter especificada y tiene una longitud especificada. |
| [**WindowsTrimStringEnd**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Quita todas las apariciones del final de un conjunto de caracteres especificado de la cadena de origen. |
| [**WindowsTrimStringStart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Quita todas las apariciones iniciales de un conjunto de caracteres especificado de la cadena de origen. |



 

 

 
