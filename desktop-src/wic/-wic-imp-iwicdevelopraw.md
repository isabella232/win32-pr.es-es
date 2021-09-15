---
description: Implementación de IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementación de IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467934"
---
# <a name="implementing-iwicdevelopraw"></a>Implementación de IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

La [**interfaz IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expone opciones de procesamiento específicas del procesamiento de imágenes sin procesar. Todos los códecs sin formato deben admitir la **interfaz IWICDevelopRaw.** Es posible que algunos códecs sin formato no puedan admitir todas las configuraciones expuestas por esta interfaz, pero debe admitir todas las configuraciones que el códec es capaz de realizar. Como mínimo, cada códec sin formato debe implementar los [**métodos SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) [**y SetRenderMode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode)

Además, algunos métodos e interfaces que son opcionales para otros códecs se recomiendan encarecidamente para códecs sin formato. Estos incluyen los [**métodos GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) y [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) en la clase descodificador de nivel de contenedor y la interfaz [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la clase de descodificación de nivel de marco.

Configuración establecer mediante los métodos [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) debe conservarse mediante el códec de forma coherente con la forma en que se conservan otros metadatos, pero nunca debe sobrescribir la configuración original de "Como toma". Al conservar los metadatos e implementar [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) y [**GetCurrentParameterSet,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)permite que las aplicaciones de procesamiento sin procesar recuperen y apliquen la configuración de procesamiento entre sesiones.

Un propósito principal de la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) es permitir que los desarrolladores de aplicaciones compilen una interfaz de usuario para ajustar los parámetros sin procesar que funcionarán de la forma más coherente posible en diferentes códecs. Supongamos que un usuario final ajustará los parámetros mediante un control deslizante, con sus valores mínimo y máximo asignados a los intervalos mínimo y máximo para el parámetro. Para admitir esto, debe hacer todo lo posible por tratar todos los intervalos de parámetros como lineales. Para asegurarse de que los controles deslizantes no sean demasiado sensibles, también debe admitir un intervalo lo más amplio posible para cada parámetro, que abarca al menos el 50 % del intervalo máximo posible. Por ejemplo, si el intervalo máximo posible de contraste va de gris puro a negro y blanco puro, con el valor predeterminado asignado a 0,0, el intervalo mínimo admitido por un códec sería de al menos la mitad entre el valor predeterminado y el gris puro en el extremo bajo (–1,0), a al menos a la mitad entre el valor predeterminado y el blanco y negro puro en el extremo superior (+1,0).


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
-   [Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointVin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
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

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) devuelve el conjunto de funcionalidades admitidas para este archivo sin formato. La [**estructura WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) se define de la siguiente manera:


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



La [**enumeración WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) usada en esta estructura se define como:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



El campo final es una [**enumeración WICRawRotationCapabilities,**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) definida como:


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

[**LoadParameterSet permite**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) al usuario especificar si se debe usar la configuración de As Shot, usar la configuración ajustada por el usuario o solicitar al descodificador que corrija automáticamente la imagen.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) devuelve un **objeto IPropertyBag2** con el conjunto de parámetros actual. A continuación, el autor de la llamada puede pasar este parámetro establecido al codificador para usarlo como opciones del codificador.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) y [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indican la compensación de exposición que se aplicará a la salida final. El intervalo válido para EV es de -5,0 a +5,0 paradas.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointVin

Todas estas funciones proporcionan maneras de obtener y establecer el punto blanco, ya sea como un valor RGB, un valor preestablecido denominado o como un valor de Kelvin. El intervalo aceptable para Kelvin es de 1500 a 30 000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) y [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indican la cantidad de contraste que se aplicará a la salida. El intervalo válido para especificar el contraste es de –1,0 a +1,0, siendo el contraste predeterminado 0,0.

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) y [**SetGamma indican**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) la gamma que se aplicará. El intervalo válido para Gamma es de 0,2 a 5,0, siendo 1,0 el valor predeterminado. Gamma normalmente se implementa mediante la función de energía gamma tradicional (una función de energía lineal con ganancia de unidad). El brillo aumenta con el aumento de Gamma y disminuye a medida que Gamma se aproxima a cero. (Tenga en cuenta que el valor mínimo es distinto de cero, porque cero daría lugar a un error de división por cero en los cálculos gamma tradicionales. El límite mínimo lógico es 1/máx., por lo que el mínimo es 0,2).

### <a name="setgetsharpness"></a>Set/GetSharpness

[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) [**y SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indican la cantidad de ajuste que se debe aplicar. El intervalo válido es de –1.0 a +1.0, siendo 0.0 la cantidad predeterminada de ajuste y –1.0 que indica que no hay ningún ajuste.

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation y**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indican la cantidad de saturación que se aplicará. El intervalo válido para especificar la saturación es de –1,0 a +1,0, siendo 0,0 la saturación normal, –1,0 que representa la desaturación completa y +1,0 que representa la saturación completa.

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) y [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indican el tono que se debe aplicar, en un sesgo verde/biaso de green/biat. El intervalo válido es de -1,0 a +1,0, con verde en el lado negativo de la escala y de color rojo en el positivo. La escala de tono se define como ortogonal a temperatura de color.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) y [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indican la cantidad de reducción de ruido que se aplicará. El intervalo válido para es –1,0 a +1,0, con 0,0 que indica la cantidad predeterminada de reducción de ruido, –1,0 que indica que no hay reducción de ruido y +1,0 que indica la reducción máxima del ruido.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) especifica el perfil de color que se va a aplicar a la imagen. Puede llamar a [**GetColorContexts para**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) recuperar el perfil de color actual.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) y [**SetToneCurve especifican**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) la curva de tono que se aplicará. Suponga la interpolación lineal entre puntos. **pToneCurve** es una estructura [**WICRawToneCurve,**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) que contiene una matriz de estructuras [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) y un recuento del número de puntos de la matriz.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



[**WiCRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contiene un valor de entrada y un valor de salida.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Cuando el autor de la llamada pasa **NULL** en el parámetro *pToneCurve,* debe devolver el tamaño necesario para [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) en el parámetro *pwActualToneCurveBufferSize.*

### <a name="setgetrotation"></a>Set/GetRotation

[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) y [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indican el grado de rotación que se aplicará. Una rotación de 90,0 especificaría una rotación de 90 grados en el sentido de las agujas del reloj. (La diferencia entre usar **SetRotation** y establecer la rotación mediante el método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) es que el códec debe conservar el conjunto de ángulos de rotación mediante **SetRotation,** mientras que establecer la rotación mediante **CopyPixels** solo gira la imagen en memoria.

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) y [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indican el nivel de calidad de salida que requiere el autor de la llamada. Cuando un usuario ajusta los parámetros, la aplicación debe mostrar una aproximación muy rápida de cómo será la imagen real si se aplican los cambios. Para este fin, la imagen normalmente se muestra en la resolución de pantalla o menos, en lugar de la resolución de imagen real, para proporcionar comentarios inmediatos al usuario. Aquí es cuando una aplicación solicita la calidad del modo borrador, por lo que debería ser muy rápido. Cuando el usuario ha realizado todos los cambios, los ha vista previamente en modo borrador y ha decidido descodificar la imagen completa con la configuración actual, la aplicación solicita un descodificación de mejor calidad. Normalmente, esto también se solicita para imprimir. Cuando se requiere un equilibrio razonable entre la velocidad y la calidad, la aplicación solicita calidad normal.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback registra una**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) función de devolución de llamada para que el descodificador llame cuando cambie cualquiera de los parámetros de procesamiento sin procesar. La firma de [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) solo tiene un método, denominado [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** tiene un único parámetro, que es una máscara que indica cuál de los parámetros de procesamiento sin procesar ha cambiado.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Se realiza una operación OR en los valores siguientes para NotificationMask.


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

**Conceptual**
</dt> <dt>

[Implementación de IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implementación de un WIC-Enabled encoder](-wic-implementingwicencoder.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



