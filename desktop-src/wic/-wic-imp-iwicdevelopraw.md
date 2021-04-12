---
description: Implementación de IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementación de IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279377"
---
# <a name="implementing-iwicdevelopraw"></a><span data-ttu-id="e6fa3-103">Implementación de IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="e6fa3-103">Implementing IWICDevelopRaw</span></span>

## <a name="iwicdevelopraw"></a><span data-ttu-id="e6fa3-104">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="e6fa3-104">IWICDevelopRaw</span></span>

<span data-ttu-id="e6fa3-105">La interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expone opciones de procesamiento específicas del procesamiento de imágenes sin procesar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-105">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface exposes processing options specific to raw image processing.</span></span> <span data-ttu-id="e6fa3-106">Todos los códecs sin formato deben admitir la interfaz **IWICDevelopRaw** .</span><span class="sxs-lookup"><span data-stu-id="e6fa3-106">All raw codecs must support the **IWICDevelopRaw** interface.</span></span> <span data-ttu-id="e6fa3-107">Es posible que algunos códecs sin formato no admitan todas las opciones de configuración expuestas por esta interfaz, pero debe admitir todos los valores de configuración que pueda realizar el códec.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-107">Some raw codecs may not be able to support every setting exposed by this interface, but you should support all the settings that your codec is capable of performing.</span></span> <span data-ttu-id="e6fa3-108">Como mínimo, cada códec sin formato debe implementar los métodos [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) y [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .</span><span class="sxs-lookup"><span data-stu-id="e6fa3-108">At minimum, every raw codec must implement the [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) methods.</span></span>

<span data-ttu-id="e6fa3-109">Además, se recomienda encarecidamente que se recomienden algunos métodos e interfaces que sean opcionales para los códecs sin formato.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-109">Additionally, some methods and interfaces that are optional for other codecs are strongly recommended for raw codecs.</span></span> <span data-ttu-id="e6fa3-110">Entre ellos se incluyen los métodos [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) y [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) en la clase descodificador de nivel de contenedor y la interfaz [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la clase descodificar en el nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-110">These include the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) and [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) methods on the container-level decoder class, and the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface on the frame-level decode class.</span></span>

<span data-ttu-id="e6fa3-111">La configuración establecida mediante el uso de los métodos [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) debe ser conservada por el códec de manera coherente con la manera en que se conservan los demás metadatos, pero nunca debe sobrescribir la configuración original de "as Shot".</span><span class="sxs-lookup"><span data-stu-id="e6fa3-111">Settings set by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) methods should be persisted by the codec in a way that’s consistent with the way other metadata is persisted, but you should never overwrite the original "As Shot" settings.</span></span> <span data-ttu-id="e6fa3-112">Al conservar los metadatos e implementar [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) y [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), las aplicaciones de procesamiento sin formato se habilitan para recuperar y aplicar la configuración de procesamiento entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-112">By persisting the metadata and implementing [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) and [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), you enable raw processing applications to retrieve and apply processing settings across sessions.</span></span>

<span data-ttu-id="e6fa3-113">El propósito principal de la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) es permitir a los desarrolladores de aplicaciones crear una interfaz de usuario para ajustar los parámetros sin formato que funcionarán de la manera más uniforme posible entre distintos códecs.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-113">A main purpose of the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface is to enable application developers to build a user interface for adjusting raw parameters that will work as consistently as possible across different codecs.</span></span> <span data-ttu-id="e6fa3-114">Suponga que un usuario final ajustará los parámetros con un control deslizante, con sus valores mínimo y máximo asignados a los intervalos mínimo y máximo para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-114">Assume that an end user will adjust the parameters by using a slider control, with its minimum and maximum values mapped to the minimum and maximum ranges for the parameter.</span></span> <span data-ttu-id="e6fa3-115">Para admitir esto, debe hacer todo lo posible para tratar todos los intervalos de parámetros como lineales.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-115">To support this, you should make every effort to treat all parameter ranges as linear.</span></span> <span data-ttu-id="e6fa3-116">Para asegurarse de que los controles deslizantes no sean sensiblemente confidenciales, también debe admitir el mayor alcance posible para cada parámetro, lo que abarca al menos el 50 por ciento del intervalo máximo posible.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-116">To ensure that the slider controls aren’t overly sensitive, you should also support as broad a range as possible for each parameter, covering at least 50 percent of the maximum possible range.</span></span> <span data-ttu-id="e6fa3-117">Por ejemplo, si el intervalo máximo posible de contraste es de gris puro a blanco y negro puros, con el valor predeterminado que se asigna a 0,0, el intervalo mínimo admitido por un códec sería de al menos la mitad del valor predeterminado y el gris puro en el extremo inferior (-1,0), al menos medio entre el valor predeterminado y el negro puro y blanco del extremo superior (+ 1,0).</span><span class="sxs-lookup"><span data-stu-id="e6fa3-117">For example, if the maximum possible range of contrast is from pure gray to pure black and white, with the default value being mapped to 0.0, the minimum range supported by a codec would be from at least halfway between the default value and pure gray on the low end (–1.0), to at least halfway between the default value and pure black and white on the high end (+1.0).</span></span>


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [<span data-ttu-id="e6fa3-118">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="e6fa3-118">QueryRawCapabilitiesInfo</span></span>](#queryrawcapabilitiesinfo)
-   [<span data-ttu-id="e6fa3-119">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fa3-119">LoadParameterSet</span></span>](#loadparameterset)
-   [<span data-ttu-id="e6fa3-120">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fa3-120">GetCurrentParameterSet</span></span>](#getcurrentparameterset)
-   [<span data-ttu-id="e6fa3-121">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="e6fa3-121">Set/GetExposureCompensation</span></span>](#setgetexposurecompensation)
-   [<span data-ttu-id="e6fa3-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="e6fa3-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [<span data-ttu-id="e6fa3-123">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="e6fa3-123">Set/GetContrast</span></span>](#setgetcontrast)
-   [<span data-ttu-id="e6fa3-124">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="e6fa3-124">Set/GetGamma</span></span>](#setgetgamma)
-   [<span data-ttu-id="e6fa3-125">Set/GetSharpness</span><span class="sxs-lookup"><span data-stu-id="e6fa3-125">Set/GetSharpness</span></span>](#setgetsharpness)
-   [<span data-ttu-id="e6fa3-126">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="e6fa3-126">Set/GetSaturation</span></span>](#setgetsaturation)
-   [<span data-ttu-id="e6fa3-127">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="e6fa3-127">Set/GetTint</span></span>](#setgettint)
-   [<span data-ttu-id="e6fa3-128">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="e6fa3-128">Set/GetNoiseReduction</span></span>](#setgetnoisereduction)
-   [<span data-ttu-id="e6fa3-129">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="e6fa3-129">SetDestinationColorContext</span></span>](#setdestinationcolorcontext)
-   [<span data-ttu-id="e6fa3-130">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="e6fa3-130">Set/GetToneCurve</span></span>](#setgettonecurve)
-   [<span data-ttu-id="e6fa3-131">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="e6fa3-131">Set/GetRotation</span></span>](#setgetrotation)
-   [<span data-ttu-id="e6fa3-132">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="e6fa3-132">Set/GetRenderMode</span></span>](#setgetrendermode)
-   [<span data-ttu-id="e6fa3-133">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="e6fa3-133">SetNotificationCallback</span></span>](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a><span data-ttu-id="e6fa3-134">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="e6fa3-134">QueryRawCapabilitiesInfo</span></span>

<span data-ttu-id="e6fa3-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) devuelve el conjunto de capacidades admitidas para este archivo sin formato.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) returns the set of supported capabilities for this raw file.</span></span> <span data-ttu-id="e6fa3-136">La estructura [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e6fa3-136">The [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) structure is defined as follows:</span></span>


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



<span data-ttu-id="e6fa3-137">La enumeración [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) usada en esta estructura se define como:</span><span class="sxs-lookup"><span data-stu-id="e6fa3-137">The [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) enumeration used in this structure is defined as:</span></span>


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



<span data-ttu-id="e6fa3-138">El campo final es una enumeración [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , que se define como:</span><span class="sxs-lookup"><span data-stu-id="e6fa3-138">The final field is a [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) enumeration, defined as:</span></span>


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a><span data-ttu-id="e6fa3-139">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fa3-139">LoadParameterSet</span></span>

<span data-ttu-id="e6fa3-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) permite al usuario especificar si desea usar como configuración de la captura, usar la configuración ajustada por el usuario o solicitar al descodificador que corrija automáticamente la imagen.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) enables the user to specify whether to use As Shot settings, use user-adjusted settings, or request the decoder to auto-correct the image.</span></span>


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a><span data-ttu-id="e6fa3-141">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fa3-141">GetCurrentParameterSet</span></span>

<span data-ttu-id="e6fa3-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) devuelve un **IPropertyBag2** con el conjunto de parámetros actual.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) returns an **IPropertyBag2** with the current parameter set.</span></span> <span data-ttu-id="e6fa3-143">A continuación, el llamador puede pasar este conjunto de parámetros al codificador para utilizarlo como las opciones del codificador.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-143">The caller can then pass this parameter set to the encoder to use as the encoder options.</span></span>

### <a name="setgetexposurecompensation"></a><span data-ttu-id="e6fa3-144">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="e6fa3-144">Set/GetExposureCompensation</span></span>

<span data-ttu-id="e6fa3-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) y [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indican la compensación de exposición que se va a aplicar a la salida final.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) and [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicate the exposure compensation to apply to the final output.</span></span> <span data-ttu-id="e6fa3-146">El intervalo válido para EV es de – 5,0 a + 5,0 se detiene.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-146">The valid range for EV is –5.0 to +5.0 stops.</span></span>

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a><span data-ttu-id="e6fa3-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="e6fa3-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>

<span data-ttu-id="e6fa3-148">Todas estas funciones proporcionan formas de obtener y establecer el punto blanco, ya sea como un valor RGB, un valor con nombre preestablecido o como un valor Kelvin.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-148">These functions all provide ways to get and set the white point, either as an RGB value, a preset named value, or as a Kelvin value.</span></span> <span data-ttu-id="e6fa3-149">El intervalo aceptable para Kelvin es 1.500 – 30.000.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-149">The acceptable range for Kelvin is 1,500 – 30,000.</span></span>

### <a name="setgetcontrast"></a><span data-ttu-id="e6fa3-150">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="e6fa3-150">Set/GetContrast</span></span>

<span data-ttu-id="e6fa3-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) y [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indican la cantidad de contraste que se va a aplicar a la salida.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) and [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicate the amount of contrast to apply to the output.</span></span> <span data-ttu-id="e6fa3-152">El intervalo válido para especificar el contraste es de – 1,0 a + 1,0, con el contraste predeterminado de 0,0.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-152">The valid range to specify contrast is –1.0 to +1.0, with the default contrast being 0.0.</span></span>

### <a name="setgetgamma"></a><span data-ttu-id="e6fa3-153">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="e6fa3-153">Set/GetGamma</span></span>

<span data-ttu-id="e6fa3-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) y [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indican el gamma que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) and [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicate the Gamma to apply.</span></span> <span data-ttu-id="e6fa3-155">El intervalo válido para gamma es de 0,2 a 5,0, y 1,0 es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-155">The valid range for Gamma is 0.2 to 5.0, with 1.0 being the default.</span></span> <span data-ttu-id="e6fa3-156">Gamma normalmente se implementa mediante la función de potencia gamma tradicional (una función de potencia lineal con ganancia de Unity).</span><span class="sxs-lookup"><span data-stu-id="e6fa3-156">Gamma typically is implemented using the traditional Gamma power function (a linear power function with unity gain).</span></span> <span data-ttu-id="e6fa3-157">El brillo aumenta con un incremento de gamma y se reduce a medida que la gamma se aproxima a cero.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-157">Brightness is increased with increasing Gamma and decreased as Gamma approaches zero.</span></span> <span data-ttu-id="e6fa3-158">(Tenga en cuenta que el valor mínimo es distinto de cero, porque cero daría como resultado un error de división por cero en los cálculos de gamma tradicionales.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-158">(Note that the minimum value is non-zero, because zero would result in a divide-by-zero error in traditional Gamma calculations.</span></span> <span data-ttu-id="e6fa3-159">El límite mínimo lógico es 1/Max, que es el motivo por el que el mínimo es 0,2).</span><span class="sxs-lookup"><span data-stu-id="e6fa3-159">The logical minimum limit is 1/max, which is why the minimum is 0.2.)</span></span>

### <a name="setgetsharpness"></a><span data-ttu-id="e6fa3-160">Set/GetSharpness</span><span class="sxs-lookup"><span data-stu-id="e6fa3-160">Set/GetSharpness</span></span>

<span data-ttu-id="e6fa3-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) y [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indican la cantidad de enfoque que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) and [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicate the amount of sharpening to apply.</span></span> <span data-ttu-id="e6fa3-162">El intervalo válido es de – 1,0 a + 1,0, donde 0,0 es la cantidad de enfoque predeterminada y – 1,0, que indica que no se realiza ningún enfoque.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-162">The valid range is –1.0 to +1.0, with 0.0 being the default amount of sharpening, and –1.0 indicating no sharpening at all.</span></span>

### <a name="setgetsaturation"></a><span data-ttu-id="e6fa3-163">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="e6fa3-163">Set/GetSaturation</span></span>

<span data-ttu-id="e6fa3-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) y [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indican la cantidad de saturación que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) and [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicate the amount of saturation to apply.</span></span> <span data-ttu-id="e6fa3-165">El intervalo válido para especificar la saturación es de – 1,0 a + 1,0, donde 0,0 es la saturación normal, – 1,0 que representa una desaturación completa y + 1,0 que representa la saturación completa.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-165">The valid range to specify saturation is –1.0 to +1.0, with 0.0 being normal saturation, –1.0 representing complete desaturation, and +1.0 representing full saturation.</span></span>

### <a name="setgettint"></a><span data-ttu-id="e6fa3-166">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="e6fa3-166">Set/GetTint</span></span>

<span data-ttu-id="e6fa3-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) y [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indican el matiz que se va a aplicar, en una diferencia de color verde/magenta.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) and [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicate the tint to apply, on a green/magenta bias.</span></span> <span data-ttu-id="e6fa3-168">El intervalo válido es de – 1,0 a + 1,0, donde el color verde está en el lado negativo de la escala y el magenta en el positivo.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-168">The valid range is –1.0 to +1.0, with green being on the negative side of the scale and magenta on the positive.</span></span> <span data-ttu-id="e6fa3-169">La escala del matiz se define como ortogonal a temperatura de color.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-169">The tint scale is defined as orthogonal to color temperature.</span></span>

### <a name="setgetnoisereduction"></a><span data-ttu-id="e6fa3-170">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="e6fa3-170">Set/GetNoiseReduction</span></span>

<span data-ttu-id="e6fa3-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) y [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indican la cantidad de reducción de ruido que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) and [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicate the amount of noise reduction to apply.</span></span> <span data-ttu-id="e6fa3-172">El intervalo válido es de – 1,0 a + 1,0, con 0,0 que indica la cantidad predeterminada de reducción de ruido, – 1,0, que indica que no hay reducción de ruido y + 1,0 indica una reducción máxima del ruido.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-172">The valid range to is –1.0 to +1.0, with 0.0 indicating the default amount of noise reduction, –1.0 indicating no noise reduction and +1.0 indicating maximum noise reduction.</span></span>

### <a name="setdestinationcolorcontext"></a><span data-ttu-id="e6fa3-173">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="e6fa3-173">SetDestinationColorContext</span></span>

<span data-ttu-id="e6fa3-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) especifica el perfil de color que se va a aplicar a la imagen.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifies the color profile to apply to the image.</span></span> <span data-ttu-id="e6fa3-175">Puede llamar a [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) para recuperar el perfil de color actual.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-175">You can call [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) to retrieve the current color profile.</span></span>

### <a name="setgettonecurve"></a><span data-ttu-id="e6fa3-176">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="e6fa3-176">Set/GetToneCurve</span></span>

<span data-ttu-id="e6fa3-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) y [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) especifican la curva de tono que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) and [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specify the tone curve to apply.</span></span> <span data-ttu-id="e6fa3-178">Asuma la interpolación lineal entre los puntos.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-178">Assume linear interpolation between points.</span></span> <span data-ttu-id="e6fa3-179">**PToneCurve** es una estructura [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , que contiene una matriz de estructuras [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) , y un recuento del número de puntos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-179">The **pToneCurve** is a [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) structure, which contains an array of [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) structures, and a count of the number of points in the array.</span></span>


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



<span data-ttu-id="e6fa3-180">Un [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contiene un valor de entrada y un valor de salida.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-180">A [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contains an input value and an output value.</span></span>


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



<span data-ttu-id="e6fa3-181">Cuando el autor de la llamada pasa **null** en el parámetro *pToneCurve* , debe devolver el tamaño necesario para el [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) en el parámetro *pcbActualToneCurveBufferSize* .</span><span class="sxs-lookup"><span data-stu-id="e6fa3-181">When the caller passes **NULL** in the *pToneCurve* parameter, you should pass back the required size for the [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) in the *pcbActualToneCurveBufferSize* parameter.</span></span>

### <a name="setgetrotation"></a><span data-ttu-id="e6fa3-182">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="e6fa3-182">Set/GetRotation</span></span>

<span data-ttu-id="e6fa3-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indican el grado de giro que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) and [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicate the degree of rotation to apply.</span></span> <span data-ttu-id="e6fa3-184">Un giro de 90,0 especificaría un giro de 90 grados en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-184">A rotation of 90.0 would specify a rotation of 90 degrees clockwise.</span></span> <span data-ttu-id="e6fa3-185">(La diferencia entre el uso de **SetRotation** y la configuración de la rotación con el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) es que el códec que se establece mediante **SetRotation** debe persistir por el códec, mientras que si se establece la rotación mediante **copyPixels** solo se gira la imagen en la memoria.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-185">(The difference between using **SetRotation** and setting rotation using the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method is that the rotation angle set using **SetRotation** should be persisted by the codec, while setting rotation through **CopyPixels** only rotates the image in memory.</span></span>

### <a name="setgetrendermode"></a><span data-ttu-id="e6fa3-186">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="e6fa3-186">Set/GetRenderMode</span></span>

<span data-ttu-id="e6fa3-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) y [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indican el nivel de calidad de la salida que requiere el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicate the quality level of output the caller requires.</span></span> <span data-ttu-id="e6fa3-188">Cuando un usuario está ajustando parámetros, la aplicación debe mostrar una aproximación muy rápida del aspecto que tendrá la imagen real si se aplican los cambios.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-188">When a user is adjusting parameters, the application should display a very fast approximation of what the actual image will look like if the changes are applied.</span></span> <span data-ttu-id="e6fa3-189">En este caso, la imagen se muestra normalmente en la resolución de pantalla o menos, en lugar de la resolución de imagen real, para proporcionar comentarios inmediatos al usuario.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-189">For this purpose, the image is usually displayed at screen resolution or less, rather than the actual image resolution, to provide immediate feedback to the user.</span></span> <span data-ttu-id="e6fa3-190">Esto se debe a que una aplicación solicitaría la calidad del modo de borrador, por lo que debería ser muy rápida.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-190">This is when an application would request Draft Mode quality, so this should be very fast.</span></span> <span data-ttu-id="e6fa3-191">Cuando el usuario ha realizado todos los cambios, los ha previsualizado en modo de borrador y ha decidido descodificar la imagen completa con la configuración actual, la aplicación solicita una descodificación de la mejor calidad.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-191">When the user has made all changes, previewed them in draft mode, and decided to decode the full image with the current settings, the application requests a Best Quality decode.</span></span> <span data-ttu-id="e6fa3-192">Normalmente, esto se solicita también para la impresión.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-192">This is usually also requested for printing.</span></span> <span data-ttu-id="e6fa3-193">Cuando se requiere un equilibrio razonable entre la velocidad de una calidad, la aplicación solicita calidad normal.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-193">Where a reasonable tradeoff between speed an quality is required, the application requests Normal Quality.</span></span>


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a><span data-ttu-id="e6fa3-194">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="e6fa3-194">SetNotificationCallback</span></span>

<span data-ttu-id="e6fa3-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registra una función de devolución de llamada para que el descodificador llame cuando cambie cualquiera de los parámetros de procesamiento sin procesar.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registers a callback function for the decoder to call when any of the Raw processing parameters change.</span></span> <span data-ttu-id="e6fa3-196">La firma de [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) tiene solo un método, llamado [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span><span class="sxs-lookup"><span data-stu-id="e6fa3-196">The signature for the [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) has only one method, called [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span></span> <span data-ttu-id="e6fa3-197">**Notify** tiene un único parámetro, que es una máscara que indica cuál de los parámetros de procesamiento sin procesar ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-197">**Notify** has a single parameter, which is a mask that indicates which of the raw processing parameters have changed.</span></span>


```C++
HRESULT Notify ( UINT NotificationMask );
```



<span data-ttu-id="e6fa3-198">Se realiza una operación OR en los siguientes valores para NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="e6fa3-198">An OR operation is performed on the following values for the NotificationMask.</span></span>


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a><span data-ttu-id="e6fa3-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6fa3-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e6fa3-200">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e6fa3-200">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6fa3-201">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="e6fa3-201">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

<span data-ttu-id="e6fa3-202">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e6fa3-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6fa3-203">Implementación de IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="e6fa3-203">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="e6fa3-204">Implementación de un codificador WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e6fa3-204">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="e6fa3-205">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e6fa3-205">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="e6fa3-206">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="e6fa3-206">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



