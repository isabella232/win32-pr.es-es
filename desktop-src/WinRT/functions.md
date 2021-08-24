---
description: Referencia de las Windows C++ en tiempo de ejecución.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: Funciones (Windows runtime)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: fbf0d4ce350251e1c13d1f6a3ff03c95068558098eac722979bc77499a094c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795015"
---
# <a name="functions-windows-runtime-c-reference"></a>Funciones (referencia Windows C++ en tiempo de ejecución)

## <a name="in-this-section"></a>En esta sección



| Función | Descripción |
|-|-|
| [**CoDecodeProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Busca la implementación de una interfaz de modelo de objetos componentes (COM) en un proceso de servidor dada una interfaz a un objeto proxy. |
| [**CreateControlInput**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Crea un [**objeto ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) en el subproceso de interfaz de usuario del autor de la llamada. |
| [**CreateControlInputEx**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Crea un [**objeto ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) en un subproceso de trabajo o en el subproceso de interfaz de usuario.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Crea una instancia de IDirect3DDevice a partir de un IDXGIDevice. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Crea una instancia de IDirect3DSurface a partir de IDXGISurface. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Crea una instancia de [IDirect3DDevice a](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) partir de [un IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice). |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Crea una instancia de [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) a partir de [IDXGISurface.](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) |
| [**CreateRandomAccessStreamOnFile**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | Crea una secuencia Windows acceso aleatorio en tiempo de ejecución para un archivo. |
| [**CreateRandomAccessStreamOverStream**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | Crea una secuencia Windows acceso aleatorio en tiempo de ejecución en torno a una implementación base [**de IStream.**](/windows/win32/api/objidl/nn-objidl-istream) |
| [**CreateStreamOverRandomAccessStream**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | Crea un [**objeto IStream**](/windows/win32/api/objidl/nn-objidl-istream) alrededor de Windows objeto [**IRandomAccessStream en**](/previous-versions//hh438400(v=vs.85)) tiempo de ejecución. |
| [**CreateXamlUIPresenter**](createxamluipresenter.md) | Una función de creador estático que puede crear un [**elemento XamlUIPresenter para**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) una superficie de representación en una aplicación de escritorio. |
| [**DbgRaiseAssertionFailure**](/previous-versions//jj635749(v=vs.85)) | Genera una aserción para la depuración.  |
| [**GetDXGIInterface(IDirect3DDevice^, DXGI_TYPE**)**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Recupera una interfaz DXGI de una [instancia de IDirect3DDevice.](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) |
| [**GetDXGIInterface(IDirect3DSurface^, DXGI_TYPE**)**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Recupera una interfaz DXGI de una [instancia de IDirect3DSurface.](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) |
| [**GetDXGIInterfaceFromObject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Recupera una interfaz DXGI de un objeto . |
| [**GetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Obtiene el objeto de información de error restringido establecido por una llamada anterior a [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) en el subproceso lógico actual. |
| [**HSTRING \_ UserFree**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Libera recursos en el lado servidor cuando los llaman los archivos de código auxiliar RPC. |
| [**HSTRING \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Libera recursos en el lado servidor cuando los llaman los archivos de código auxiliar RPC.  |
| [**HSTRING \_ UserMarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Serializa un objeto [**HSTRING**](hstring.md) en el búfer RPC. |
| [**HSTRING \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Serializa un objeto [**HSTRING**](hstring.md) en el búfer RPC. |
| [**HSTRING \_ UserSize**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Calcula el tamaño del cable del [**objeto HSTRING**](hstring.md) y obtiene su identificador y los datos. |
| [**HSTRING \_ UserSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Calcula el tamaño del cable del [**objeto HSTRING**](hstring.md) y obtiene su identificador y los datos. |
| [**HSTRING \_ UserUnmarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Desmarshals un [**objeto HSTRING**](hstring.md) del búfer RPC. |
| [**HSTRING \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Desmarshals un [**objeto HSTRING**](hstring.md) del búfer RPC. |
| [**IsErrorPropagationEnabled**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | Indica si se produce el evento [**CoreApplication.UnhandledErrorDetected**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) para los errores devueltos por el delegado registrado como una función de devolución de llamada para un evento de api en tiempo de ejecución de Windows o la finalización de un método asincrónico. |
| [**DllGetActivationFactory**](/previous-versions//br205771(v=vs.85)) | Recupera el generador de activación de un archivo DLL que contiene clases activables Windows runtime. |
| [**MetaDataGetDispenser**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Crea una clase de dispensador. |
| [**PdfCreateRenderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Obtiene una instancia de la [**interfaz IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) para mostrar una sola página de un archivo Portable Document Format (PDF). |
| [**PdfRenderParams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Rellena una [**\_ escoba de \_ PARAMS RENDER**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) en PDF. Una estructura RENDER PARAMS de PDF \_ representa un conjunto de propiedades para generar una sola página de un archivo \_ PDF. |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | Activa la clase Windows runtime especificada. |
| [**RoCaptureErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Guarda el contexto de error actual para que esté disponible para las llamadas posteriores a la [**función RoFailFastWithErrorContext.**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) |
| [**RoClearError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Quita la información de error existente del bloque de entorno de subprocesos (TEB) actual. |
| [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Genera una excepción no continuable en el proceso actual. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Genera una excepción no continuable en el proceso actual y también permite incluir contextos de error adicionales que el sistema operativo aún no ha capturado. |
| [**RoFreeParameterizedTypeExtra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Libera el identificador asignado por [**RoGetParameterizedTypeInstanceIID.**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) |
| [**RoGetActivatableClassRegistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Permite recuperar información de registro de clases. |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Obtiene el generador de activación para la clase en tiempo de ejecución especificada. |
| [**RoGetEtoleReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Crea una referencia ágil para un objeto especificado por la interfaz especificada. |
| [**RoGetChevIdentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Obtiene un identificador único para el apartamento actual. |
| [**RoGetBufferMarsbuffer**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Proporciona un serializador de IBuffer estándar para implementar la semántica asociada a la interfaz IBuffer cuando se serializa. |
| [**RoGetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | Obtiene el comportamiento actual de los informes de Windows de error en tiempo de ejecución. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Busca y recupera el archivo de metadatos que describe la interfaz binaria de aplicación (ABI) para el typename especificado. |
| [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Calcula el identificador de interfaz (IID) del tipo de interfaz o delegado que se produce cuando se crea una instancia de una interfaz o un delegado con parámetros con los argumentos de tipo especificados. |
| [**RoGetServerActivatableClasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Recupera las clases activables registradas para un servidor ejecutable determinado (EXE), que se registró en el identificador de paquete del proceso de llamada. |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | Inicializa el Windows runtime en el subproceso actual con el modelo de simultaneidad especificado. |
| [**RoInspectThreadErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Obtiene el objeto de error que representa la pila de llamadas en el punto donde se originó el error. |
| [**RoInspectCapturedStackBackTrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Proporciona una manera de que los depuradores inspeccionen una pila de llamadas desde un proceso de destino. |
| [**RoOriginateError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Notifica un error y una cadena informativa a un depurador asociado. |
| [**RoOriginateErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Notifica un error y una cadena informativa a un depurador asociado. |
| [**RoOriginateLanguageException**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Notifica un error, una cadena informativa y un objeto de error a un depurador asociado. |
| [**RoParameterizedTypeExtraGetTypeSignature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Obtiene la firma de tipo utilizada para calcular el IID de la última llamada a [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) con el identificador especificado. |
| [**RoParseTypeName**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Analiza un nombre de tipo y los parámetros de tipo existentes, en el caso de los tipos con parámetros. |
| [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | Registra una matriz de generadores de activación fuera de proceso para un servidor Windows runtime. |
| [**RoRegisterForHutShutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Registra una [**devolución de llamada IHutShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) que se invocará cuando se cierre el apartamento actual. |
| [**RoReportUnhandledError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Desencadena el controlador de errores global cuando se produce una excepción no controlada. |
| [**RoReportFailedDelegate**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Desencadena el controlador de errores global cuando se produce un error de delegado. |
| [**RoResolveNamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | Determine los elementos secundarios directos, tipos y sub namespaces del espacio de nombres Windows Runtime especificado, a partir de cualquier lenguaje de programación compatible con Windows Runtime. |
| [**RoResolveRestrictedErrorInfoReference**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Devuelve el [**puntero de interfaz IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) basado en la referencia dada. |
| [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | Quita una matriz de generadores de activación registrados de Windows Runtime. |
| [**RoSetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | Establece el comportamiento de informes de las Windows de error en tiempo de ejecución. |
| [**RoTransformError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Notifica un error modificado y una cadena informativa a un depurador asociado. |
| [**RoTransformErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Notifica un error transformado y una cadena informativa a un depurador asociado. |
| [**RoUninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | Cierra el Windows runtime en el subproceso actual. |
| [**RoUnregisterForHutShutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Anula el registro de una interfaz [**IHutShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) registrada previamente. |
| [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Establece el objeto de información de error restringido para el subproceso actual. |
| [**WindowsCompareStringOrdinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Compara dos objetos [**HSTRING**](hstring.md) especificados y devuelve un entero que indica su posición relativa en un criterio de ordenación. |
| [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Concatena dos cadenas especificadas. |
| [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Crea un [**nuevo HSTRING**](hstring.md) basado en la cadena de origen especificada. |
| [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Crea una nueva referencia de cadena basada en la cadena especificada. |
| [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Disminuye el recuento de referencias de un búfer de cadena. |
| [**WindowsDeleteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Descarta un búfer de cadena asignado previamente si no se promovió a [**HSTRING.**](hstring.md) |
| [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Crea una copia de la cadena especificada. |
| [**WindowsGetStringLen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Obtiene la longitud, en caracteres Unicode, de la cadena especificada. |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Obtiene el búfer de respaldo de la cadena especificada. |
| [**WindowsInspectString**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | Proporciona una manera de que los depuradores muestren el valor de un [**HSTRING**](hstring.md) en tiempo de ejecución de Windows en otro espacio de direcciones, de forma remota o desde un volcado de memoria.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | Proporciona una manera de que los depuradores muestren el valor de un [**HSTRING**](hstring.md) en tiempo de ejecución de Windows en otro espacio de direcciones, de forma remota o desde un volcado de memoria.  |
| [**WindowsIsStringEmpty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Indica si la cadena especificada es la cadena vacía. |
| [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Asigna un búfer de caracteres mutable para su uso en [**la creación de HSTRING.**](hstring.md) |
| [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Crea un [**HSTRING a**](hstring.md) partir del búfer [**de HSTRING \_ especificado.**](hstring-buffer.md) |
| [**WindowsReplaceString**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Reemplaza todas las apariciones de un conjunto de caracteres de la cadena especificada por otro conjunto de caracteres para crear una nueva cadena. |
| [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Indica si la cadena especificada tiene caracteres NULL incrustados. |
| [**WindowsSubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Recupera una subcadena de la cadena especificada. La subcadena comienza en la posición de carácter especificada. |
| [**WindowsSubstringWithSpecifiedLength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Recupera una subcadena de la cadena especificada. La subcadena comienza en una posición de carácter especificada y tiene una longitud especificada. |
| [**WindowsTrimStringEnd**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Quita todas las apariciones finales de un conjunto especificado de caracteres de la cadena de origen. |
| [**WindowsTrimStringStart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Quita todas las apariciones iniciales de un conjunto especificado de caracteres de la cadena de origen. |



 

 

 
