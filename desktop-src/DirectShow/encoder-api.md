---
description: Encoder API
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: Encoder API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b97dc2242cc718605a851186c726e3301493b7637b94e88b7987868741874a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823645"
---
# <a name="encoder-api"></a>Encoder API

Encoder API proporciona una interfaz uniforme para configurar codificadores de software y hardware. Las aplicaciones pueden usar Encoder API para configurar un codificador y almacenar los valores de configuración. Los proveedores de codificadores pueden usar Encoder API para exponer las funcionalidades de un codificador. Aunque Encoder API está diseñado principalmente para codificadores, es lo suficientemente general como para que los descodificadores también puedan admitirla.

Encoder API se expone a las aplicaciones a través de la [**interfaz ICodecAPI,**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) que se expone mediante el filtro del codificador. El filtro del codificador puede ser un filtro DirectShow nativo, un codificador de hardware o un objeto multimedia DirectX (DMO).

-   Filtros de software: un codificador que se implementa como filtro de DirectShow nativo debe exponer [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directamente.
-   Codificadores de hardware: el dispositivo de codificación se expone a través de uno o varios minidriveres AVStream, que KSProxy representa en modo de usuario. KSProxy traduce las llamadas al método [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) en conjuntos de propiedades KS. Para más información, consulte la documentación de DDK.
-   DDO: el DMO debe exponer la [**interfaz ICodecAPI.**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) DirectShow aplicaciones pueden consultar el filtro DMO Wrapper, que expone la interfaz agregando el DMO. Las aplicaciones que no se basan DirectShow pueden consultar el DMO directamente.

### <a name="encoder-capabilties"></a>Capacidades del codificador

Un codificador puede registrar una lista de funcionalidades de alto nivel almacenándolos en el registro del sistema. Cada funcionalidad se identifica mediante un GUID. Para enumerar las funcionalidades de un codificador determinado, haga lo siguiente:

1.  Cree el moniker que representa el filtro del codificador. (Consulte [Uso del enumerador de dispositivos del sistema).](using-the-system-device-enumerator.md)
2.  Consulte el moniker de filtro para la [**interfaz IGetCapabilitiesKey.**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey)
3.  Llame [**a IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey). El método devuelve un identificador a la clave del Registro que contiene la lista de funcionalidades del filtro.
4.  Llame a **la función RegEnumValue** para enumerar los valores de la clave devuelta.

Si va a desadichar un codificador, cree las entradas del Registro para las funcionalidades cuando se registre el filtro. Para los filtros de software, cree una clave denominada **Capabilities** que sea adyacente a las claves **FilterData** **y FriendlyName.** Normalmente, agregaría esta información después de llamar [**a AMovieDllRegisterServer2 para**](amoviedllregisterserver2.md) registrar los datos de filtro estándar. Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md). Como alternativa, puede crear una clave **CapabilitiesLocation** que contenga una cadena que da la ubicación de la clave **Capabilities** en el Registro. La cadena debe comenzar por \\ "HKLM", "HKCR" o \\ "HKCU" para \\ indicar el subárbol del Registro. Para Plug and Play dispositivos, los archivos de instalación del controlador deben crear una clave **Capabilities** adyacente a la clave **FriendlyName** del filtro, o bien puede usar una clave **CapabilitiesLocation** como se describe para los filtros de software.

Una vez que haya creado la **clave Funcionalidades,** cree un valor para cada GUID de funcionalidad. El nombre del valor debe ser el formato de cadena del GUID, con el formato `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Cada tipo de valor debe ser uno de los siguientes:

-   Valor numérico único. Use un **valor DWORD.**
-   GUID. Use el formato de cadena del GUID.
-   Pares numéricos. Use una cadena con la forma "a,b" para representar pares de valores, como ancho y alto, o numerador y denominador para fracciones.
-   Matrices de valores. Use varias cadenas **(REG \_ SZ \_ MULTI)** para representar más de un valor.

En el ejemplo siguiente se muestra el diseño del Registro para un filtro de software:


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Perfiles de codificador

Un *perfil de codificador* es una lista fija de opciones de configuración que se pueden aplicar a un codificador en tiempo de ejecución. Los perfiles son independientes del codificador; una aplicación puede seleccionar un codificador y, a continuación, seleccionar un perfil y aplicar la configuración del perfil al codificador. Los perfiles se identifican mediante GUID y deben almacenarse en la siguiente ubicación en el Registro:


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



where *Profile GUID (GUID de perfil)*

es la forma de cadena del GUID que identifica el perfil. Cree valores para cada configuración. Cree también un valor de cadena denominado "FriendlyName" cuyos datos identifiquen el perfil (por ejemplo, "LowBandwidthVideo").

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de codificadores y descodificadores](encoder-and-decoder-development.md)
</dt> </dl>

 

 



