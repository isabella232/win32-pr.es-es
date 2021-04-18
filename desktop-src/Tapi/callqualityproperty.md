---
description: 'Los métodos ITCallQualityControl:: GetRange, ITCallQualityControl:: get y ITCallQualityControl:: set usan la enumeración CallQualityProperty para indicar la propiedad de calidad de la llamada que se va a resolver.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Enumeración CallQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680403"
---
# <a name="callqualityproperty-enumeration"></a>Enumeración CallQualityProperty

\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Los métodos [**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl:: get**](itcallqualitycontrol-get.md)y [**ITCallQualityControl:: set**](itcallqualitycontrol-set.md) usan la enumeración **CallQualityProperty** para indicar la propiedad de calidad de la llamada que se va a resolver.

## <a name="syntax"></a>Sintaxis


```C++
} CallQualityProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**
</dt> <dd>

Intervalo de control.

</dd> <dt>

<span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**
</dt> <dd>

Velocidad de bits para la Conferencia.

</dd> <dt>

<span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**
</dt> <dd>

Velocidad de bits de entrada máxima.

</dd> <dt>

<span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**
</dt> <dd>

Velocidad de bits de entrada actual.

</dd> <dt>

<span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**
</dt> <dd>

Velocidad de bits de salida máxima.

</dd> <dt>

<span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**
</dt> <dd>

Velocidad de bits de salida actual.

</dd> <dt>

<span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ MaxCPULoad**
</dt> <dd>

Carga máxima de la CPU.

</dd> <dt>

<span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**
</dt> <dd>

Carga de CPU actual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl:: get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl:: set**](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




