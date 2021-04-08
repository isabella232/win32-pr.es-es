---
title: Registro de complementos de DSP
description: Registro de complementos de DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Complementos de Windows Media Player, entradas del registro
- complementos, entradas del registro
- Complementos de procesamiento de señal digital, entradas del registro
- Complementos DSP, entradas del registro
- registro, Complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994953"
---
# <a name="registering-dsp-plug-ins"></a>Registro de complementos de DSP

Para que el complemento de DSP esté disponible en Windows Media Player debe crear las siguientes subclaves y entradas del registro en el equipo del usuario.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos del complemento DSP. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PluginClsid*             | GUID que es el identificador de clase de la clase principal del complemento DSP. Esta es la clase que implementa **IMediaObject**, **IPluginEnable** y posiblemente **ISpecifyPropertyPages**. En un complemento de modo dual, esta clase también implementa **IMFTransform** y **IMFGetService**. Este GUID debe estar en formato de registro, completar con las llaves.<br/> Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/> |
| *PluginClassFriendlyName* | Un nombre descriptivo para la clase principal del complemento DSP. Ejemplo: "clase ProsewareDSP"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | Ruta de acceso completa al archivo DLL que implementa el complemento DSP. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *Subprocesamiento*               | Cadena que especifica el modelo de subprocesos para el complemento. Si el complemento va a ejecutarse con Windows Media Player 11 en Windows Vista, esta entrada del registro debe ser igual a "both". Si el complemento se va a ejecutar en Windows XP o en sistemas operativos anteriores, esta entrada del registro puede ser "Apartment" o "both".                                                                                           |



 

Si el complemento de DSP implementa una interfaz personalizada y el complemento se va a ejecutar en Windows Media Player 11 en Windows Vista, debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para nombres, valores numéricos y identificadores únicos globales (GUID) que son específicos del complemento DSP. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición           | Descripción                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | GUID que es el identificador de clase de la clase que implementa los proxies y códigos auxiliares para las interfaces personalizadas del complemento DSP. Este GUID debe estar en formato de registro, completar con las llaves.<br/> Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/> |
| *ProxyStubModuleName* | Ruta de acceso completa al archivo DLL que implementa las interfaces de proxy y de código auxiliar para el complemento DSP. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *CustomInterfaceId*   | GUID que es el identificador de interfaz de una interfaz personalizada implementada por el complemento DSP. Este GUID debe estar en formato de registro, completar con las llaves.<br/> Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/>                           |
| *CustomInterfaceName* | Nombre de una interfaz personalizada implementada por el complemento DSP. Ejemplo: "IProsewareDsp"<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | El número de métodos, incluidos los métodos heredados, definidos por una interfaz personalizada. Ejemplo: "5"<br/>                                                                                                                                                                  |



 

Si el complemento de DSP proporciona una página de propiedades, debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos del complemento DSP. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición                 | Descripción                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | GUID que es el identificador de clase de la clase de página de propiedades que proporciona el complemento DSP. Este GUID debe estar en formato de registro, completar con las llaves.<br/> Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/> |
| *PropPageClassFriendlyName* | Nombre descriptivo para la clase de página de propiedades. Ejemplo: "clase de página de propiedades ProsewareDSP"<br/>                                                                                                                                     |
| *PluginModuleName*          | Ruta de acceso completa al archivo DLL que implementa el complemento DSP. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**Llamando a IWMPPluginRegistrar**

Además de las subclaves del registro y las entradas descritas en las listas y las tablas anteriores, debe crear algunas claves y entradas del registro mediante una llamada a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin). Este método realiza el registro necesario para permitir que Windows Media Player reconozca el complemento y lo presente como una opción al usuario.

Llame a **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** en la función **DllRegisterServer** del complemento y llame a [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) en la función **DllUnregisterServer** del complemento. Para obtener un puntero a una interfaz **IWMPMediaPluginRegistrar** , llame a **COCREATEINSTANCE**, pasando CLSID \_ WMPMediaPluginRegistrar como identificador de clase. La constante \_ WMPMediaPluginRegistrar de CLSID se define en wmpservices. h.

**Registro en el Asistente para complementos de DSP**

El Asistente para complementos de DSP, que se incluye en el Windows SDK, genera código de ejemplo basado en Active Template Library (ATL). La función **DllRegisterServer** del complemento de ejemplo llama a la función **RegisterServer** de ATL, que crea subclaves del registro y entradas de acuerdo con dos archivos de script del registro en el proyecto de Visual Studio. El archivo *projectname*. RGS contiene el script para registrar la clase principal del complemento y el archivo *projectname* PropPage. RGS contiene el script para registrar la clase de página de propiedades del complemento. La función **DllRegisterServer** del complemento de ejemplo también llama a **IWMPPluginRegistrar:: WMPRegisterPlayerPlugin**.

El Asistente para complementos DSP también genera código para un componente de código auxiliar de proxy que es un archivo. dll de registro automático. El código de registro de ese archivo está en dlldata. cpp. Las **\_ rutinas** de macro DLLDATA se expanden para incluir una implementación de **DllRegisterServer**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





