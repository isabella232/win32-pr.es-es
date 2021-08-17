---
description: Interfaces (Windows runtime C++)
ms.assetid: CB05B5F8-BE15-4BE0-A651-F6E8912D649D
title: Interfaces (Windows Runtime)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 468944bcd2437309d953fe53e64e36366ca0cd7ac6ad4d8c32aa9c8d71f91ca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741649"
---
# <a name="interfaces"></a>Interfaces

## <a name="in-this-section"></a>En esta sección

| Interfaz | Descripción |
|-|-|
| [**IActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iactivatableclassregistration) | Permite obtener la información de registro de una clase. |
| [**IActivationFactory**](/windows/win32/api/activation/nn-activation-iactivationfactory) | Permite que Windows en tiempo de ejecución active las clases. |
| [**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference) | Permite recuperar una referencia ágil a un objeto . |
| [**IHutShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) | Habilita el registro de un controlador de notificaciones de cierre de apartamento. |
| [**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) | Representa el método al que se llama cuando se completa una acción asincrónica. |
| [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) | Representa una acción asincrónica. |
| [**IAsyncActionProgressHandler<TProgress>**](/previous-versions//br205782(v=vs.85)) | Representa el método al que se llama cuando una acción asincrónica notifica el progreso. |
| [**IAsyncActionWithProgress<TProgress>**](/previous-versions//br205784(v=vs.85)) | Representa una acción asincrónica que informa sobre el progreso. |
| [**IAsyncActionWithProgressCompletedHandler<TProgress>**](/previous-versions//br205785(v=vs.85)) | Representa el método al que se llama cuando se completa una acción asincrónica que informa del progreso. |
| [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) | Proporciona compatibilidad con operaciones asincrónicas. |
| [**IAsyncOperation<TResult>**](/previous-versions//br205802(v=vs.85)) | Representa una operación asincrónica que devuelve un resultado. |
| [**IAsyncOperationCompletedHandler<TResult>**](/previous-versions//br205803(v=vs.85)) | Representa el método al que se llama cuando se completa una operación asincrónica. |
| [**IAsyncOperationProgressHandler**](/previous-versions//br205805(v=vs.85)) | Representa el método al que se llama cuando una operación asincrónica notifica el progreso. |
| [**IAsyncOperationWithProgress**](/previous-versions//br205807(v=vs.85)) | Representa una operación asincrónica que devuelve un resultado e informa sobre el progreso. |
| [**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85)) | Representa el método al que se llama cuando se completa una operación asincrónica que informa del progreso. |
| [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative) | Representa un marco de datos de audio. |
| [**IAudioFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenativefactory) | Crea instancias de [**IAudioFrameNative.**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative) |
| [**IBuffer**](/previous-versions//hh438362(v=vs.85)) | Representa una matriz de bytes. |
| [**IBufferByteAccess**](/previous-versions//hh846267(v=vs.85)) | Representa un búfer como una matriz de bytes. |
| [**IClosable**](/windows/win32/api/windows.foundation/nn-windows-foundation-iclosable) | Define un método para liberar los recursos asignados. |
| [**ICompositionDrawingSurfaceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) | Interfaz de interoperación nativa que permite dibujar en un objeto de superficie mediante un RECT para definir el área en la que dibujar. |
| [**ICompositionDrawingSurfaceInterop2**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2) | Interfaz de interoperación nativa que permite leer el contenido de una superficie de dibujo de composición (o una superficie de dibujo virtual de composición). |
| [**ICompositionGraphicsDeviceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiongraphicsdeviceinterop) | Interfaz de interoperación nativa que permite obtener y establecer el dispositivo gráfico. |
| [**IContactManagerInterop**](/previous-versions//dn302109(v=vs.85)) | Habilita el acceso [**a los métodos contactManager**](/uwp/api/Windows.ApplicationModel.Contacts.ContactManager?view=winrt-19041) en una aplicación que administra varias ventanas. |
| [**ICoreApplication**](/previous-versions//hh438365(v=vs.85)) | Permite que las aplicaciones controlen los cambios de estado, administren ventanas e integren con una variedad de marcos de interfaz de usuario. |
| [**ICoreApplicationExit**](/previous-versions//hh438366(v=vs.85)) | Proporciona los medios para que las Windows store dejen de ejecutarse. |
| [**ICoreApplicationInitialization**](/previous-versions//hh438370(v=vs.85)) | Contiene un método de ejecución que se usa para iniciar el objeto de aplicación desde el punto de entrada de una aplicación. |
| [**ICoreApplicationView**](/previous-versions//hh438372(v=vs.85)) | Representa una vista de una aplicación. |
| [**ICoreImmersiveApplication**](/previous-versions//hh438382(v=vs.85)) | Contiene métodos para administrar vistas en una aplicación. |
| [**ICoreInputInterop**](/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop) | Habilita un origen de entrada en Windows objeto CoreInput de la aplicación [**store.**](https://www.bing.com/search?q=**CoreInput**) |
| [**ICoreWindowInterop**](/windows/desktop/api/corewindow/nn-corewindow-icorewindowinterop) | Permite a las aplicaciones obtener el identificador de ventana de la ventana [**(CoreWindow)**](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041)asociada a esta interfaz. |
| [**IDllServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration) | Permite obtener la información de registro de un servidor en proceso. |
| [**IErrorReportingSettings**](/previous-versions//br205818(v=vs.85)) | Proporciona la integración del depurador para Windows runtime. |
| [**IEventHandler<T>**](/previous-versions//hh438385(v=vs.85)) | Representa el método que controlará un evento que tiene datos de evento de tipo **T**. |
| [**IExeServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration) | Permite obtener la información de registro de un servidor fuera de proceso. |
| [**IExeServerRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserverregistration) | Representa un servidor fuera de proceso registrado. |
| [**IFindReferenceTargetsCallback**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback) | Define la interfaz para las devoluciones de llamada de [**IReferenceTracker::FindTrackerTargets.**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets) La implementación de esta interfaz debe pasar cualquier [**instancia de IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) que encuentre al **método FoundTrackerTarget.** |
| [**IInputPaneInterop**](/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop) | Habilita el acceso a los miembros de la [**clase InputPane**](/uwp/api/Windows.UI.ViewManagement.InputPane?view=winrt-19041) en una aplicación de escritorio. |
| [**IInputStream**](/previous-versions//hh438387(v=vs.85)) | Permite obtener una operación de lector asincrónica en un flujo secuencial de bytes. |
| [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) | Proporciona la funcionalidad necesaria para todas las Windows runtime. |
| [**IIterable<T>**](/previous-versions//br205825(v=vs.85)) | Expone el iterador , que admite una iteración simple sobre una colección de un tipo especificado. |
| [**IIterator<T>**](/previous-versions//br205827(v=vs.85)) | Admite la iteración en una colección. |
| [**IKeyValuePair<K, V>**](/previous-versions//br205831(v=vs.85)) | Representa un par clave-valor. |
| [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo) | Permite recuperar el [**puntero IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) almacenado en la información de error con la llamada a RoOriginateLanguageException. |
| [**ILanguageExceptionErrorInfo2**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2) | Permite que las proyecciones de lenguaje proporcionen y recuperen información de error como [**con ILanguageExceptionErrorInfo,**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo)con la ventaja adicional de trabajar a través de los límites del lenguaje. |
| [**ILanguageExceptionTransform**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform) | Permite que las proyecciones de lenguaje estén disponibles para el sistema en cualquier contexto de una excepción que se produce desde el contexto de un controlador catch que detecta una excepción diferente. |
| [**ILanguageExceptionStackBackTrace**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace) | Permite que las proyecciones proporcionen un seguimiento de pila personalizado para esa excepción. |
| [**IMap<K, V>**](/previous-versions//br205834(v=vs.85)) | Representa una colección asociativa. |
| [**IMapChangedEventArgs<K>**](/previous-versions//br205835(v=vs.85)) | Proporciona datos para un [**evento MapChanged.**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) |
| [**IMapView<K, V>**](/previous-versions//br205838(v=vs.85)) | Representa una vista inmutable en [**un objeto IMap(K,V).**](/previous-versions//br205834(v=vs.85)) |
| [**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85)) | Proporciona acceso a [**un IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) como una matriz de bytes. |
| [**IMetaDataAssemblyImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport) | Proporciona métodos para acceder al contenido de un manifiesto del ensamblado y examinarlo. |
| [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) | Proporciona métodos para crear un nuevo ámbito de metadatos o abrir uno existente. |
| [**IMetaDataDispenserEx**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenserex) | Extiende la interfaz [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) para proporcionar la capacidad de controlar cómo funcionan las API de metadatos en el ámbito de metadatos actual. |
| [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) | Proporciona métodos para importar y manipular los metadatos existentes desde un archivo portable ejecutable (PE) u otro origen, como una biblioteca de tipos o un archivo binario de metadatos independiente en tiempo de ejecución. |
| [**IMetaDataImport2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport2) | Extiende la [**interfaz IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) para proporcionar la capacidad de trabajar con tipos genéricos. |
| [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) | Proporciona métodos para el almacenamiento y la recuperación de información de metadatos en tablas. |
| [**IMetaDataTables2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables2) | Extiende [**IMetaDataTables para**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) incluir métodos para trabajar con flujos de metadatos. |
| [**IObservableMap<K, V>**](/previous-versions//br205851(v=vs.85)) | Notifica a los controladores de eventos los cambios dinámicos en un mapa, como cuando se agregan o quitan elementos. |
| [**IObservableVector<T>**](/previous-versions//br205854(v=vs.85)) | Notifica a los controladores de eventos los cambios en el vector. |
| [**IOplockBreakingHandler**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-ioplockbreakinghandler) | Esta interfaz no está implementada actualmente. |
| [**IOutputStream**](/previous-versions//hh438390(v=vs.85)) | Permite obtener una operación de escritura asincrónica en un flujo secuencial de bytes. |
| [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) | Representa una API de alto rendimiento para mostrar una sola página de un archivo de formato de documento portable (PDF). |
| [**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85)) | Permite a los desarrolladores del depurador controlar el ciclo de vida de una Windows store, por ejemplo, cuando se suspende o se reanuda. |
| [**IPlayToManagerInterop**](/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop) | Permite el acceso [**a los métodos PlayToManager**](/uwp/api/Windows.Media.PlayTo.PlayToManager?view=winrt-19041) en una Windows store que administra varias ventanas. |
| [**IPrintManagerInterop**](/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop) | Habilita el acceso [**a los métodos PrintManager**](/uwp/api/Windows.Graphics.Printing.PrintManager?view=winrt-19041) en una Windows Store que administra varias ventanas. |
| [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) | Representa un valor en un almacén de Windows runtime. |
| [**IPropertyValueStatics**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics) | Crea [**objetos IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) que puede almacenar en un almacén de propiedades. |
| [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) | Permite obtener un lector de bytes asincrónico o un escritor de bytes que se coloca en la ubicación especificada en una secuencia de bytes de acceso aleatorio. |
| [**IRandomAccessStreamFileAccessMode**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-irandomaccessstreamfileaccessmode) | Proporciona acceso al modo de acceso a archivos que se usó cuando se llamó al método [**StorageFile.OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) para abrir la secuencia de bytes de acceso aleatorio. |
| [**IReference<T>**](/previous-versions//br224583(v=vs.85)) | Permite extender el sistema de Windows runtime para enumeraciones, estructuras y tipos delegados definidos por el usuario. |
| [**IReferenceArray<T>**](/previous-versions//br224584(v=vs.85)) | Permite extender el sistema de propiedades Windows Runtime para matrices de enumeraciones, estructuras y tipos delegados definidos por el usuario. |
| [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) | Define la interfaz implementada por el marco XAML para administrar referencias a objetos XAML. |
| [**IReferenceTrackerHost**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost) | Define una interfaz que proporciona los servicios globales utilizados por el sistema de recolección de elementos no utilizados (GC) utilizado por el marco XAML. |
| [**IReferenceTrackerManager**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager) | Define la interfaz para un administrador de referencias de objetos XAML. Implemente esta interfaz para administrar instancias de [**IReferenceTracker en**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) objetos XAML. |
| [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) | Define una interfaz implementada por un objeto recolector de elementos no utilizados al que se hace referencia desde XAML. |
| [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) | Representa los detalles de un error, incluida la información de error restringida. |
| [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) | Representa un mapa de bits de software. |
| [**ISoftwareBitmapNativeFactory**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory) | Crea instancias de [**ISoftwareBitmapNative.**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) |
| [**IStorageFolderHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istoragefolderhandleaccess) | Proporciona acceso al identificador del sistema operativo de una carpeta de almacenamiento. |
| [**IStorageItemHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istorageitemhandleaccess) | Proporciona acceso al identificador del sistema operativo de un archivo de almacenamiento. |
| [**IStringable**](/windows/win32/api/windows.foundation/nn-windows-foundation-istringable) | Proporciona una manera de representar el objeto actual como una cadena. |
| [**ISurfaceImageSourceManagerNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative) | Permite realizar operaciones masivas en todos los [**objetos SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) creados en el mismo proceso. |
| [**ISurfaceImageSourceNativeWithD2D**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d) | Proporciona la implementación de una superficie compartida de Microsoft DirectX que se muestra en [**SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) o [**VirtualSurfaceImageSource.**](/uwp/api/Windows.UI.Xaml.Media.Imaging.VirtualSurfaceImageSource?view=winrt-19041) |
| [**ISurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative) | Proporciona la implementación de una superficie de tamaño fijo compartida para el dibujo de Direct2D. |
| [**ISuspendingDeferral**](isuspendingdeferral.md) | Administra una operación de suspensión de aplicaciones retrasada. |
| [**ISuspendingEventArgs**](isuspendingeventargs.md) | Proporciona datos para un evento de suspensión de aplicaciones. |
| [**ISuspendingOperation**](isuspendingoperation.md) | Proporciona información sobre una operación de suspensión de aplicaciones. |
| [**ISwapChainBackgroundPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative) | Proporciona interoperación entre XAML y una cadena de intercambio de DirectX. |
| [**ISwapChainPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative) | Proporciona interoperación entre XAML y una cadena de intercambio de DirectX. A [**diferencia de SwapChainBackgroundPanel,**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041) **un SwapChainPanel** puede aparecer en cualquier nivel del árbol de presentación XAML y puede haber más de 1 en cualquier árbol determinado. |
| [**ISwapChainPanelNative2**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2) | Proporciona interoperación entre XAML y una cadena de intercambio de DirectX. A [**diferencia de SwapChainBackgroundPanel,**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041) **un SwapChainPanel** puede aparecer en cualquier nivel del árbol de presentación XAML y puede haber más de 1 en cualquier árbol determinado. |
| [**ITypedEventHandler<TSender, TArgs>**](/previous-versions//hh438424(v=vs.85)) | Representa el método que controlará un evento de un remitente de tipo **TSender** y datos de evento de tipo **T**. |
| [**IUnbufferedFileHandleOplockCallback**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback) | Define un método de devolución de llamada que desea ejecutar cuando se rompe el bloqueo oportunista de un identificador que se obtiene mediante una llamada al método [**IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle.**](/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle) |
| [**IUnbufferedFileHandleProvider**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleprovider) | Proporciona acceso a los identificadores de una secuencia de bytes de acceso aleatorio que [**creó el método StorageFile.OpenAsync.**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) |
| [**IVector<T>**](/previous-versions//br224590(v=vs.85)) | Representa una colección de elementos de acceso aleatorio. |
| [**IVectorChangedEventArgs**](ivectorchangedeventargs.md) | Proporciona datos para un [**evento VectorChanged.**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) |
| [**IVectorView<T>**](/previous-versions//br224594(v=vs.85)) | Representa una vista inmutable en [**un IVector(T).**](/uwp/api/windows.foundation.collections.ivector-1?view=winrt-19041) |
| [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) | Representa un fotograma de datos de vídeo. |
| [**IVideoFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenativefactory) | Crea instancias de [**IVideoFrameNative.**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) |
| [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) | Representa una vista en una aplicación. |
| [**IViewProviderFactory**](/previous-versions//hh438427(v=vs.85)) | Crea una instancia de vistas que implementan la [**interfaz IViewProvider.**](/previous-versions//hh438426(v=vs.85)) |
| [**IVirtualSurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) | Proporciona la implementación de una superficie compartida grande (mayor que el tamaño de pantalla) para el dibujo de DirectX. |
| [**IVirtualSurfaceUpdatesCallbackNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative) | Proporciona una interfaz para la implementación de comportamientos de dibujo cuando [**un elemento VirtualSurfaceImageSource**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) solicita una actualización. |
| [**IWeakReference**](/windows/win32/api/weakreference/nn-weakreference-iweakreference) | Representa una referencia débil a un objeto . |
| [**IWeakReferenceSource**](/windows/win32/api/weakreference/nn-weakreference-iweakreferencesource) | Representa un objeto de origen al que se puede recuperar una referencia débil. |
| [**MapChangedEventHandler<K, V>**](/previous-versions//br224612(v=vs.85)) | Representa el método que controla el [**evento MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) de un mapa observable. |
| [**VectorChangedEventHandler<T>**](/previous-versions//br224626(v=vs.85)) | Representa el método que controla el [**evento VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) de un vector observable. |
