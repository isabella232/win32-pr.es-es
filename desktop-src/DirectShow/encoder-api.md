---
description: API del codificador
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API del codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423040"
---
# <a name="encoder-api"></a>API del codificador

La API del codificador proporciona una interfaz uniforme para configurar el software y los codificadores de hardware. Las aplicaciones pueden usar la API del codificador para configurar un codificador y almacenar los valores de configuración. Los proveedores del codificador pueden usar la API del codificador para exponer las capacidades de un codificador. Aunque la API del codificador está diseñada principalmente para los codificadores, es lo suficientemente general para que los descodificadores también lo admitan.

La API del codificador se expone a las aplicaciones a través de la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , que se expone mediante el filtro del codificador. El filtro del codificador puede ser un filtro DirectShow nativo, un codificador de hardware o un objeto multimedia DirectX (DMO).

-   Filtros de software: un codificador que se implementa como un filtro DirectShow nativo debe exponer el [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directamente.
-   Codificadores de hardware: el dispositivo de codificación se expone a través de uno o varios AVStream los minicontroladores, que se representan en modo usuario por KSProxy. KSProxy convierte las llamadas al método [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) en conjuntos de propiedades KS. Para obtener más información, consulte la documentación de DDK.
-   DMOs: DMO debe exponer la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) . Las aplicaciones de DirectShow pueden consultar el filtro de contenedor de DMO, que expone la interfaz mediante la agregación de DMO. Las aplicaciones no basadas en DirectShow pueden consultar el DMO directamente.

### <a name="encoder-capabilties"></a>Codificador funcionalidades

Un codificador puede registrar una lista de capacidades de alto nivel almacenándola en el registro del sistema. Cada función se identifica mediante un GUID. Para enumerar las capacidades de un codificador determinado, haga lo siguiente:

1.  Cree el moniker que representa el filtro del codificador. (Consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md)).
2.  Consulte el moniker de filtro para la interfaz [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .
3.  Llame a [**IGetCapabilitiesKey:: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey). El método devuelve un identificador para la clave del registro que contiene la lista de capacidades del filtro.
4.  Llame a la función **RegEnumValue** para enumerar los valores de la clave devuelta.

Si está devloping un codificador, cree las entradas del registro para las capacidades cuando se registre el filtro. En el caso de los filtros de software, cree una clave denominada **Capabilities** que sea adyacente a las claves **FilterData** y **FriendlyName** . Normalmente, se agrega esta información después de llamar a [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) para registrar los datos de filtro estándar. Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md). Como alternativa, puede crear una clave **CapabilitiesLocation** que contenga una cadena que proporcione la ubicación de la clave **Capabilities** en el registro. La cadena debe comenzar por "HKLM \\ ", "HKCR \\ " o "HKCU \\ " para indicar el subárbol del registro. En el caso de los dispositivos Plug and Play, los archivos de instalación del controlador deben crear una clave de **funcionalidad** junto a la clave **FriendlyName** del filtro, o bien puede usar una clave **CapabilitiesLocation** , como se describe en filtros de software.

Una vez que haya creado la clave **capacidades** , cree un valor para cada GUID de funcionalidad. El nombre del valor debe ser el formato de cadena del GUID, en el formulario `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Cada tipo de valor debe ser uno de los siguientes:

-   Valor numérico único. Use un valor **DWORD** .
-   GUID. Use el formato de cadena del GUID.
-   Pares numéricos. Use una cadena con el formato "a, b" para representar pares de valores, como el ancho y el alto, o el numerador y el denominador para fracciones.
-   Matrices de valores. Use cadenas múltiples (**reg \_ SZ \_ multi**) para representar más de un valor.

En el ejemplo siguiente se muestra el diseño del registro para un filtro de software:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Perfiles del codificador

Un *Perfil de codificador* es una lista fija de valores de configuración que se puede aplicar a un codificador en tiempo de ejecución. Los perfiles son independientes del codificador; una aplicación puede seleccionar un codificador y, a continuación, seleccionar un perfil y aplicar la configuración del perfil al codificador. Los perfiles se identifican por GUID y deben almacenarse en la siguiente ubicación del registro:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



Where ( *GUID de perfil* )

es la forma de cadena del GUID que identifica el perfil. Cree valores para cada configuración. Cree también un valor de cadena denominado "FriendlyName" cuyos datos identifiquen el perfil (por ejemplo, "LowBandwidthVideo").

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo del codificador y descodificador](encoder-and-decoder-development.md)
</dt> </dl>

 

 



