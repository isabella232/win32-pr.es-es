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
# <a name="encoder-api"></a><span data-ttu-id="5d306-103">API del codificador</span><span class="sxs-lookup"><span data-stu-id="5d306-103">Encoder API</span></span>

<span data-ttu-id="5d306-104">La API del codificador proporciona una interfaz uniforme para configurar el software y los codificadores de hardware.</span><span class="sxs-lookup"><span data-stu-id="5d306-104">The Encoder API provides a uniform interface for configuring software and hardware encoders.</span></span> <span data-ttu-id="5d306-105">Las aplicaciones pueden usar la API del codificador para configurar un codificador y almacenar los valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="5d306-105">Applications can use the Encoder API to configure an encoder and to store the configuration settings.</span></span> <span data-ttu-id="5d306-106">Los proveedores del codificador pueden usar la API del codificador para exponer las capacidades de un codificador.</span><span class="sxs-lookup"><span data-stu-id="5d306-106">Encoder vendors can use the Encoder API to expose the capabilities of an encoder.</span></span> <span data-ttu-id="5d306-107">Aunque la API del codificador está diseñada principalmente para los codificadores, es lo suficientemente general para que los descodificadores también lo admitan.</span><span class="sxs-lookup"><span data-stu-id="5d306-107">Although the Encoder API is designed primarily for encoders, it is general enough that decoders can support it as well.</span></span>

<span data-ttu-id="5d306-108">La API del codificador se expone a las aplicaciones a través de la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , que se expone mediante el filtro del codificador.</span><span class="sxs-lookup"><span data-stu-id="5d306-108">The Encoder API is exposed to applications through the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface, which is exposed by the encoder filter.</span></span> <span data-ttu-id="5d306-109">El filtro del codificador puede ser un filtro DirectShow nativo, un codificador de hardware o un objeto multimedia DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="5d306-109">The encoder filter may be a native DirectShow filter, a hardware encoder, or a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="5d306-110">Filtros de software: un codificador que se implementa como un filtro DirectShow nativo debe exponer el [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directamente.</span><span class="sxs-lookup"><span data-stu-id="5d306-110">Software filters: An encoder that is implemented as a native DirectShow filter should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directly.</span></span>
-   <span data-ttu-id="5d306-111">Codificadores de hardware: el dispositivo de codificación se expone a través de uno o varios AVStream los minicontroladores, que se representan en modo usuario por KSProxy.</span><span class="sxs-lookup"><span data-stu-id="5d306-111">Hardware encoders: The encoding device is exposed through one or more AVStream minidrivers, which are represented in user mode by KSProxy.</span></span> <span data-ttu-id="5d306-112">KSProxy convierte las llamadas al método [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) en conjuntos de propiedades KS.</span><span class="sxs-lookup"><span data-stu-id="5d306-112">KSProxy translates [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) method calls into KS property sets.</span></span> <span data-ttu-id="5d306-113">Para obtener más información, consulte la documentación de DDK.</span><span class="sxs-lookup"><span data-stu-id="5d306-113">For more information, see the DDK documentation.</span></span>
-   <span data-ttu-id="5d306-114">DMOs: DMO debe exponer la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="5d306-114">DMOs: The DMO should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="5d306-115">Las aplicaciones de DirectShow pueden consultar el filtro de contenedor de DMO, que expone la interfaz mediante la agregación de DMO.</span><span class="sxs-lookup"><span data-stu-id="5d306-115">DirectShow applications can query the DMO Wrapper filter, which exposes the interface by aggregating the DMO.</span></span> <span data-ttu-id="5d306-116">Las aplicaciones no basadas en DirectShow pueden consultar el DMO directamente.</span><span class="sxs-lookup"><span data-stu-id="5d306-116">Applications not based on DirectShow can query the DMO directly.</span></span>

### <a name="encoder-capabilties"></a><span data-ttu-id="5d306-117">Codificador funcionalidades</span><span class="sxs-lookup"><span data-stu-id="5d306-117">Encoder Capabilties</span></span>

<span data-ttu-id="5d306-118">Un codificador puede registrar una lista de capacidades de alto nivel almacenándola en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d306-118">An encoder can register a list of high-level capabilities by storing them in the system registry.</span></span> <span data-ttu-id="5d306-119">Cada función se identifica mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="5d306-119">Each capability is identified by a GUID.</span></span> <span data-ttu-id="5d306-120">Para enumerar las capacidades de un codificador determinado, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5d306-120">To enumerate the capabilities of a particular encoder, do the following:</span></span>

1.  <span data-ttu-id="5d306-121">Cree el moniker que representa el filtro del codificador.</span><span class="sxs-lookup"><span data-stu-id="5d306-121">Create the moniker that represents the encoder filter.</span></span> <span data-ttu-id="5d306-122">(Consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md)).</span><span class="sxs-lookup"><span data-stu-id="5d306-122">(See [Using the System Device Enumerator](using-the-system-device-enumerator.md).)</span></span>
2.  <span data-ttu-id="5d306-123">Consulte el moniker de filtro para la interfaz [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .</span><span class="sxs-lookup"><span data-stu-id="5d306-123">Query the filter moniker for the [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) interface.</span></span>
3.  <span data-ttu-id="5d306-124">Llame a [**IGetCapabilitiesKey:: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="5d306-124">Call [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span></span> <span data-ttu-id="5d306-125">El método devuelve un identificador para la clave del registro que contiene la lista de capacidades del filtro.</span><span class="sxs-lookup"><span data-stu-id="5d306-125">The method returns a handle to the registry key that contains the filter's capabilities list.</span></span>
4.  <span data-ttu-id="5d306-126">Llame a la función **RegEnumValue** para enumerar los valores de la clave devuelta.</span><span class="sxs-lookup"><span data-stu-id="5d306-126">Call the **RegEnumValue** function to enumerate the values for the returned key.</span></span>

<span data-ttu-id="5d306-127">Si está devloping un codificador, cree las entradas del registro para las capacidades cuando se registre el filtro.</span><span class="sxs-lookup"><span data-stu-id="5d306-127">If you are devloping an encoder, create the registry entries for the capabilities when the filter is registered.</span></span> <span data-ttu-id="5d306-128">En el caso de los filtros de software, cree una clave denominada **Capabilities** que sea adyacente a las claves **FilterData** y **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="5d306-128">For software filters, create a key named **Capabilities** that is adjacent to the **FilterData** and **FriendlyName** keys.</span></span> <span data-ttu-id="5d306-129">Normalmente, se agrega esta información después de llamar a [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) para registrar los datos de filtro estándar.</span><span class="sxs-lookup"><span data-stu-id="5d306-129">Typically, you would add this information after calling [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) to register the standard filter data.</span></span> <span data-ttu-id="5d306-130">Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5d306-130">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="5d306-131">Como alternativa, puede crear una clave **CapabilitiesLocation** que contenga una cadena que proporcione la ubicación de la clave **Capabilities** en el registro.</span><span class="sxs-lookup"><span data-stu-id="5d306-131">Alternatively, you can create a **CapabilitiesLocation** key that contains a string giving the location of the **Capabilities** key in the registry.</span></span> <span data-ttu-id="5d306-132">La cadena debe comenzar por "HKLM \\ ", "HKCR \\ " o "HKCU \\ " para indicar el subárbol del registro.</span><span class="sxs-lookup"><span data-stu-id="5d306-132">The string should start with "HKLM\\", "HKCR\\", or "HKCU\\" to indicate the registry subtree.</span></span> <span data-ttu-id="5d306-133">En el caso de los dispositivos Plug and Play, los archivos de instalación del controlador deben crear una clave de **funcionalidad** junto a la clave **FriendlyName** del filtro, o bien puede usar una clave **CapabilitiesLocation** , como se describe en filtros de software.</span><span class="sxs-lookup"><span data-stu-id="5d306-133">For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.</span></span>

<span data-ttu-id="5d306-134">Una vez que haya creado la clave **capacidades** , cree un valor para cada GUID de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="5d306-134">Once you have created the **Capabilities** key, create a value for each capability GUID.</span></span> <span data-ttu-id="5d306-135">El nombre del valor debe ser el formato de cadena del GUID, en el formulario `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="5d306-135">The name of the value should be the string form of the GUID, in the form `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="5d306-136">Cada tipo de valor debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d306-136">Each value type should be one of the following:</span></span>

-   <span data-ttu-id="5d306-137">Valor numérico único.</span><span class="sxs-lookup"><span data-stu-id="5d306-137">Single numerical value.</span></span> <span data-ttu-id="5d306-138">Use un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5d306-138">Use a **DWORD** value.</span></span>
-   <span data-ttu-id="5d306-139">GUID.</span><span class="sxs-lookup"><span data-stu-id="5d306-139">GUID.</span></span> <span data-ttu-id="5d306-140">Use el formato de cadena del GUID.</span><span class="sxs-lookup"><span data-stu-id="5d306-140">Use the string form of the GUID.</span></span>
-   <span data-ttu-id="5d306-141">Pares numéricos.</span><span class="sxs-lookup"><span data-stu-id="5d306-141">Numeric pairs.</span></span> <span data-ttu-id="5d306-142">Use una cadena con el formato "a, b" para representar pares de valores, como el ancho y el alto, o el numerador y el denominador para fracciones.</span><span class="sxs-lookup"><span data-stu-id="5d306-142">Use a string with the form "a,b" to represent pairs of values, such as width and height, or numerator and denominator for fractions.</span></span>
-   <span data-ttu-id="5d306-143">Matrices de valores.</span><span class="sxs-lookup"><span data-stu-id="5d306-143">Arrays of values.</span></span> <span data-ttu-id="5d306-144">Use cadenas múltiples (**reg \_ SZ \_ multi**) para representar más de un valor.</span><span class="sxs-lookup"><span data-stu-id="5d306-144">Use multi-strings (**REG\_SZ\_MULTI**) to represent more than one value.</span></span>

<span data-ttu-id="5d306-145">En el ejemplo siguiente se muestra el diseño del registro para un filtro de software:</span><span class="sxs-lookup"><span data-stu-id="5d306-145">The following example shows the registry layout for a software filter:</span></span>


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a><span data-ttu-id="5d306-146">Perfiles del codificador</span><span class="sxs-lookup"><span data-stu-id="5d306-146">Encoder Profiles</span></span>

<span data-ttu-id="5d306-147">Un *Perfil de codificador* es una lista fija de valores de configuración que se puede aplicar a un codificador en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5d306-147">An *encoder profile* is a fixed list of configuration settings that can be applied to an encoder at run time.</span></span> <span data-ttu-id="5d306-148">Los perfiles son independientes del codificador; una aplicación puede seleccionar un codificador y, a continuación, seleccionar un perfil y aplicar la configuración del perfil al codificador.</span><span class="sxs-lookup"><span data-stu-id="5d306-148">Profiles are independent of the encoder; an application can select an encoder, then select a profile and apply the profile settings to the encoder.</span></span> <span data-ttu-id="5d306-149">Los perfiles se identifican por GUID y deben almacenarse en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="5d306-149">Profiles are identified by GUID and should be stored in the following location in the registry:</span></span>


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



<span data-ttu-id="5d306-150">Where ( *GUID de perfil* )</span><span class="sxs-lookup"><span data-stu-id="5d306-150">where *Profile GUID*</span></span>

<span data-ttu-id="5d306-151">es la forma de cadena del GUID que identifica el perfil.</span><span class="sxs-lookup"><span data-stu-id="5d306-151">is the string form of the GUID that identifies the profile.</span></span> <span data-ttu-id="5d306-152">Cree valores para cada configuración.</span><span class="sxs-lookup"><span data-stu-id="5d306-152">Create values for each setting.</span></span> <span data-ttu-id="5d306-153">Cree también un valor de cadena denominado "FriendlyName" cuyos datos identifiquen el perfil (por ejemplo, "LowBandwidthVideo").</span><span class="sxs-lookup"><span data-stu-id="5d306-153">Also create a string value named "FriendlyName" whose data identifies the profile (such as "LowBandwidthVideo").</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d306-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d306-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d306-155">Desarrollo del codificador y descodificador</span><span class="sxs-lookup"><span data-stu-id="5d306-155">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



