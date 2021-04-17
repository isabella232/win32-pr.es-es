---
description: 'La enumeración StreamQualityProperty que usan los métodos ITStreamQualityControl:: GetRange, ITStreamQualityControl:: get y ITStreamQualityControl:: set para indicar la propiedad de calidad de la secuencia que se está solucionando.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Enumeración StreamQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691104"
---
# <a name="streamqualityproperty-enumeration"></a>Enumeración StreamQualityProperty

\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La enumeración **StreamQualityProperty** que usan los métodos [**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl:: get**](itstreamqualitycontrol-get.md)y [**ITStreamQualityControl:: set**](itstreamqualitycontrol-set.md) para indicar la propiedad de calidad de la secuencia que se está solucionando.

## <a name="syntax"></a>Sintaxis


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**
</dt> <dd>

Velocidad de bits máxima.

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**
</dt> <dd>

Velocidad de bits mínima.

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**
</dt> <dd>

Intervalo máximo de fotogramas.

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**
</dt> <dd>

Intervalo mínimo de fotogramas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl:: get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl:: set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




