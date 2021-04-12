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
# <a name="implementing-iwicdevelopraw"></a>Implementación de IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

La interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expone opciones de procesamiento específicas del procesamiento de imágenes sin procesar. Todos los códecs sin formato deben admitir la interfaz **IWICDevelopRaw** . Es posible que algunos códecs sin formato no admitan todas las opciones de configuración expuestas por esta interfaz, pero debe admitir todos los valores de configuración que pueda realizar el códec. Como mínimo, cada códec sin formato debe implementar los métodos [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) y [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .

Además, se recomienda encarecidamente que se recomienden algunos métodos e interfaces que sean opcionales para los códecs sin formato. Entre ellos se incluyen los métodos [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) y [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) en la clase descodificador de nivel de contenedor y la interfaz [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la clase descodificar en el nivel de marco.

La configuración establecida mediante el uso de los métodos [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) debe ser conservada por el códec de manera coherente con la manera en que se conservan los demás metadatos, pero nunca debe sobrescribir la configuración original de "as Shot". Al conservar los metadatos e implementar [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) y [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), las aplicaciones de procesamiento sin formato se habilitan para recuperar y aplicar la configuración de procesamiento entre sesiones.

El propósito principal de la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) es permitir a los desarrolladores de aplicaciones crear una interfaz de usuario para ajustar los parámetros sin formato que funcionarán de la manera más uniforme posible entre distintos códecs. Suponga que un usuario final ajustará los parámetros con un control deslizante, con sus valores mínimo y máximo asignados a los intervalos mínimo y máximo para el parámetro. Para admitir esto, debe hacer todo lo posible para tratar todos los intervalos de parámetros como lineales. Para asegurarse de que los controles deslizantes no sean sensiblemente confidenciales, también debe admitir el mayor alcance posible para cada parámetro, lo que abarca al menos el 50 por ciento del intervalo máximo posible. Por ejemplo, si el intervalo máximo posible de contraste es de gris puro a blanco y negro puros, con el valor predeterminado que se asigna a 0,0, el intervalo mínimo admitido por un códec sería de al menos la mitad del valor predeterminado y el gris puro en el extremo inferior (-1,0), al menos medio entre el valor predeterminado y el negro puro y blanco del extremo superior (+ 1,0).


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



-   [QueryRawCapabilitiesInfo](#queryrawcapabilitiesinfo)
-   [LoadParameterSet](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Set/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/GetGamma](#setgetgamma)
-   [Set/GetSharpness](#setgetsharpness)
-   [Set/GetSaturation](#setgetsaturation)
-   [Set/GetTint](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/GetRotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) devuelve el conjunto de capacidades admitidas para este archivo sin formato. La estructura [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) se define de la siguiente manera:


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



La enumeración [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) usada en esta estructura se define como:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



El campo final es una enumeración [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , que se define como:


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>LoadParameterSet

[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) permite al usuario especificar si desea usar como configuración de la captura, usar la configuración ajustada por el usuario o solicitar al descodificador que corrija automáticamente la imagen.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) devuelve un **IPropertyBag2** con el conjunto de parámetros actual. A continuación, el llamador puede pasar este conjunto de parámetros al codificador para utilizarlo como las opciones del codificador.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) y [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indican la compensación de exposición que se va a aplicar a la salida final. El intervalo válido para EV es de – 5,0 a + 5,0 se detiene.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin

Todas estas funciones proporcionan formas de obtener y establecer el punto blanco, ya sea como un valor RGB, un valor con nombre preestablecido o como un valor Kelvin. El intervalo aceptable para Kelvin es 1.500 – 30.000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) y [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indican la cantidad de contraste que se va a aplicar a la salida. El intervalo válido para especificar el contraste es de – 1,0 a + 1,0, con el contraste predeterminado de 0,0.

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) y [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indican el gamma que se va a aplicar. El intervalo válido para gamma es de 0,2 a 5,0, y 1,0 es el valor predeterminado. Gamma normalmente se implementa mediante la función de potencia gamma tradicional (una función de potencia lineal con ganancia de Unity). El brillo aumenta con un incremento de gamma y se reduce a medida que la gamma se aproxima a cero. (Tenga en cuenta que el valor mínimo es distinto de cero, porque cero daría como resultado un error de división por cero en los cálculos de gamma tradicionales. El límite mínimo lógico es 1/Max, que es el motivo por el que el mínimo es 0,2).

### <a name="setgetsharpness"></a>Set/GetSharpness

[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) y [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indican la cantidad de enfoque que se va a aplicar. El intervalo válido es de – 1,0 a + 1,0, donde 0,0 es la cantidad de enfoque predeterminada y – 1,0, que indica que no se realiza ningún enfoque.

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) y [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indican la cantidad de saturación que se va a aplicar. El intervalo válido para especificar la saturación es de – 1,0 a + 1,0, donde 0,0 es la saturación normal, – 1,0 que representa una desaturación completa y + 1,0 que representa la saturación completa.

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) y [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indican el matiz que se va a aplicar, en una diferencia de color verde/magenta. El intervalo válido es de – 1,0 a + 1,0, donde el color verde está en el lado negativo de la escala y el magenta en el positivo. La escala del matiz se define como ortogonal a temperatura de color.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) y [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indican la cantidad de reducción de ruido que se va a aplicar. El intervalo válido es de – 1,0 a + 1,0, con 0,0 que indica la cantidad predeterminada de reducción de ruido, – 1,0, que indica que no hay reducción de ruido y + 1,0 indica una reducción máxima del ruido.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) especifica el perfil de color que se va a aplicar a la imagen. Puede llamar a [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) para recuperar el perfil de color actual.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) y [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) especifican la curva de tono que se va a aplicar. Asuma la interpolación lineal entre los puntos. **PToneCurve** es una estructura [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) , que contiene una matriz de estructuras [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) , y un recuento del número de puntos de la matriz.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



Un [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contiene un valor de entrada y un valor de salida.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Cuando el autor de la llamada pasa **null** en el parámetro *pToneCurve* , debe devolver el tamaño necesario para el [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) en el parámetro *pcbActualToneCurveBufferSize* .

### <a name="setgetrotation"></a>Set/GetRotation

[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indican el grado de giro que se va a aplicar. Un giro de 90,0 especificaría un giro de 90 grados en el sentido de las agujas del reloj. (La diferencia entre el uso de **SetRotation** y la configuración de la rotación con el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) es que el códec que se establece mediante **SetRotation** debe persistir por el códec, mientras que si se establece la rotación mediante **copyPixels** solo se gira la imagen en la memoria.

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) y [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indican el nivel de calidad de la salida que requiere el autor de la llamada. Cuando un usuario está ajustando parámetros, la aplicación debe mostrar una aproximación muy rápida del aspecto que tendrá la imagen real si se aplican los cambios. En este caso, la imagen se muestra normalmente en la resolución de pantalla o menos, en lugar de la resolución de imagen real, para proporcionar comentarios inmediatos al usuario. Esto se debe a que una aplicación solicitaría la calidad del modo de borrador, por lo que debería ser muy rápida. Cuando el usuario ha realizado todos los cambios, los ha previsualizado en modo de borrador y ha decidido descodificar la imagen completa con la configuración actual, la aplicación solicita una descodificación de la mejor calidad. Normalmente, esto se solicita también para la impresión. Cuando se requiere un equilibrio razonable entre la velocidad de una calidad, la aplicación solicita calidad normal.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registra una función de devolución de llamada para que el descodificador llame cuando cambie cualquiera de los parámetros de procesamiento sin procesar. La firma de [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) tiene solo un método, llamado [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** tiene un único parámetro, que es una máscara que indica cuál de los parámetros de procesamiento sin procesar ha cambiado.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Se realiza una operación OR en los siguientes valores para NotificationMask.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

**Vista**
</dt> <dt>

[Implementación de IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implementación de un codificador WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



