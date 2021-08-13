---
title: Registro de complementos DE DSP
description: Registro de complementos DE DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Reproductor de Windows Media complementos, entradas del Registro
- complementos, entradas del Registro
- complementos de procesamiento de señales digitales, entradas del Registro
- Complementos de DSP, entradas del Registro
- registro, complementos de DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7671c59dfe64094afbc5f0537bcae237b3812699f4db1a06519054b14ef295f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570385"
---
# <a name="registering-dsp-plug-ins"></a>Registro de complementos DE DSP

Para que el complemento DSP esté disponible en Reproductor de Windows Media debe crear las siguientes subclaves y entradas del Registro en el equipo del usuario.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



En la sintaxis del Registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos del complemento DSP. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PluginClsid*             | GUID que es el identificador de clase de la clase principal del complemento DSP. Esta es la clase que implementa **IMediaObject**, **IPluginEnable y,** posiblemente, **ISpecifyPropertyPages.** En un complemento de modo dual, esta clase también implementa **LANTRANSFORM Y** **EL SERVICIODEGETGET.** Este GUID debe estar en formato del Registro, con las llaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PluginClassFriendlyName* | Un nombre descriptivo para la clase principal del complemento DSP. Ejemplo: "Clase ProsewareDSP"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | Ruta de acceso completa al archivo DLL que implementa el complemento DSP. Ejemplo: "C: \\ Archivos \\ de programa Proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *Subprocesamiento*               | Cadena que especifica el modelo de subprocesos para el complemento. Si el complemento se va a ejecutar con Reproductor de Windows Media 11 en Windows Vista, esta entrada del Registro debe ser igual a "Both". Si el complemento se va a ejecutar en Windows XP o sistemas operativos anteriores, esta entrada del Registro puede ser igual a "Apartment" o "Both".                                                                                           |



 

Si el complemento DSP implementa una interfaz personalizada y si el complemento se va a ejecutar en Reproductor de Windows Media 11 en Windows Vista, debe crear las siguientes subclaves y entradas del Registro en el equipo del usuario.


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



En la sintaxis del Registro anterior, los símbolos en cursiva son marcadores de posición para nombres, valores numéricos e identificadores únicos globales (GUID) específicos del complemento DSP. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición           | Descripción                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | GUID que es el identificador de clase de la clase que implementa los servidores proxy y los códigos auxiliares para las interfaces personalizadas del complemento DSP. Este GUID debe estar en formato del Registro, con las llaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *ProxyStubModuleName* | Ruta de acceso completa al archivo DLL que implementa las interfaces de proxy y stub para el complemento DE DSP. Ejemplo: "C: \\ Archivos \\ de programa Proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *CustomInterfaceId*   | GUID que es el identificador de interfaz de una interfaz personalizada que implementa el complemento DSP. Este GUID debe estar en formato del Registro, con las llaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                           |
| *CustomInterfaceName* | Nombre de una interfaz personalizada que implementa el complemento DSP. Ejemplo: "IProsewareDsp"<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | Número de métodos, incluidos los métodos heredados, definidos por una interfaz personalizada. Ejemplo: "5"<br/>                                                                                                                                                                  |



 

Si el complemento DSP proporciona una página de propiedades, debe crear las siguientes subclaves y entradas del Registro en el equipo del usuario.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



En la sintaxis del Registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos del complemento DSP. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición                 | Descripción                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | GUID que es el identificador de clase para la clase de página de propiedades proporcionada por el complemento DSP. Este GUID debe estar en formato del Registro, con las llaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PropPageClassFriendlyName* | Nombre descriptivo de la clase de página de propiedades. Ejemplo: "Clase de página de propiedades ProsewareDSP"<br/>                                                                                                                                     |
| *PluginModuleName*          | Ruta de acceso completa al archivo DLL que implementa el complemento DSP. Ejemplo: "C: \\ Archivos \\ de programa Proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**Llamada a IWMPPluginRegistrar**

Además de las subclaves y las entradas del Registro descritas en las listas y tablas anteriores, debe crear algunas claves y entradas del Registro llamando a [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin). Este método realiza el registro necesario para permitir Reproductor de Windows Media reconocer el complemento y presentarlo como una opción al usuario.

Llame **a IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** en la función **DllRegisterServer** del complemento y llame a [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin en](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) la función **DllUnregisterServer del complemento.** Para obtener un puntero a una **interfaz IWMPMediaPluginRegistrar,** llame a **CoCreateInstance** y pase CLSID \_ WMPMediaPluginRegistrar como identificador de clase. La constante CLSID \_ WMPMediaPluginRegistrar se define en wmpservices.h.

**Registro en el Asistente para complementos de DSP**

El asistente para complementos de DSP, que se incluye en el SDK de Windows, genera código de ejemplo basado en Active Template Library (ATL). La función **DllRegisterServer** del complemento de ejemplo llama a la función **RegisterServer** de ATL, que crea subclaves y entradas del Registro según dos archivos de script del Registro del Visual Studio proyecto. El archivo *ProjectName*.rgs contiene el script para registrar la clase principal del complemento y el archivo *ProjectName* PropPage.rgs contiene el script para registrar la clase de página de propiedades del complemento. La función **DllRegisterServer** del complemento de ejemplo también llama a **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.

El asistente para complementos de DSP también genera código para un componente de código auxiliar de proxy que es un archivo .dll registro. El código de registro de ese archivo está en dlldata.cpp. La macro **DLLDATA \_ ROUTINES** se expande para incluir una implementación de **DllRegisterServer**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





