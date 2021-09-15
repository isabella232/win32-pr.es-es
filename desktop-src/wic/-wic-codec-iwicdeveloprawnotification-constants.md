---
description: Marcas usadas por IWICDevelopRawNotificationCallback para indicar qué miembros han cambiado.
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: Constantes IWICDevelopRawNotificationCallback (Wincodec.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8bf5d7cb2f4ac0e6fddd1f2e9151c95143b0cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574388"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>Constantes IWICDevelopRawNotificationCallback

Marcas usadas por [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) para indicar qué miembros han cambiado.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                            | Descripción                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**WICRawChangeNotification \_ ExposureCompensation**</dt> <dt>0x00000001</dt> </dl>             | Máscara usada para notificar un cambio de compensación de exposición.<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ NamedWhitePoint**</dt> <dt>0x00000002</dt> </dl>                                 | Máscara usada para notificar un [**cambio de WICNamedWhitePoint.**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint)<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ KelvinWhitePoint**</dt> <dt>0x00000004</dt> </dl>                             | Máscara usada para notificar un cambio de punto blanco de Kelvin.<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_ RGBWhitePoint**</dt> <dt>0x00000008</dt> </dl>                                         | Máscara usada para notificar un cambio de punto blanco RGB.<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**WICRawChangeNotification \_ Contraste**</dt> <dt>0x00000010</dt> </dl>                                                             | Máscara usada para notificar un cambio de contraste.<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**WICRawChangeNotification \_ Gamma**</dt> <dt>0x00000020</dt> </dl>                                                                         | Máscara usada para notificar un cambio gamma.<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**WICRawChangeNotification \_ Sharpness**</dt> <dt>0x00000040</dt> </dl>                                                         | Máscara que se usa para notificar un cambio de niguidad.<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**WICRawChangeNotification \_ Saturación**</dt> <dt>0x00000080</dt> </dl>                                                     | Máscara usada para notificar un cambio de saturación.<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**WICRawChangeNotification \_ Tint**</dt> <dt>0x00000100</dt> </dl>                                                                             | Máscara usada para notificar un cambio de tono.<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**WICRawChangeNotification \_ NoiseReduction**</dt> <dt>0x00000200</dt> </dl>                                     | Máscara usada para notificar un cambio de reducción de ruido.<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**WICRawChangeNotification \_ DestinationColorContext**</dt> <dt>0x00000400</dt> </dl> | Máscara usada para notificar un cambio de contexto de color de destino.<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**WICRawChangeNotification \_ ToneCurve**</dt> <dt>0x00000800</dt> </dl>                                                         | Máscara usada para notificar un cambio de curva de tono.<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**WICRawChangeNotification \_ Rotación**</dt> <dt>0x00001000</dt> </dl>                                                             | Máscara usada para notificar un [**cambio de WICRawRotationCapabilities.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities)<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**WICRawChangeNotification \_ RenderMode**</dt> <dt>0x00002000</dt> </dl>                                                     | Máscara usada para notificar un [**cambio de WICRawRenderMode.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)<br/>                     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows \[ de escritorio de Vista\]<br/>                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincodec.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 




