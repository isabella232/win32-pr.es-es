---
title: Método IAMWMBufferPassCallback Notify
description: El pin llama al método Notify para cada búfer que se entrega durante el streaming.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Notificar al método windows Media Format
- Notify method windows Media Format , IAMWMBufferPassCallback (interfaz)
- IAMWMBufferPassCallback interfaz windows Media Format , Notify (método)
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f364243e40400884287c6219698991ccf8afc0be86a85ec612a5b193253994dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847540"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>IAMWMBufferPassCallback::Notify (Método)

El pin llama al método **Notify** para cada búfer que se entrega durante el streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNSSBuffer3* \[ En\]
</dt> <dd>

Puntero a la [**interfaz INSSBuffer3 expuesta**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) en el ejemplo multimedia.

</dd> <dt>

*pPin* \[ En\]
</dt> <dd>

Puntero al pin asociado a la secuencia multimedia a la que pertenece el ejemplo.

</dd> <dt>

*prtStart* \[ En\]
</dt> <dd>

Hora de inicio del ejemplo.

</dd> <dt>

*prtEnd* \[ En\]
</dt> <dd>

Hora de finalización del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se especifica ningún valor devuelto determinado. El pin de llamada omite el **valor HRESULT**.

## <a name="remarks"></a>Comentarios

Este método permite a una aplicación examinar y actuar sobre la información del búfer multimedia antes de que se procese el contenido del búfer. La aplicación es responsable de conocer el tipo de medio en el pin. Esta información se puede obtener obteniendo primero la información de secuencia del perfil y, a continuación, llamando al método [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) para determinar qué pin está asociado a cada secuencia.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DirectShow Referencia de QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**IAMWMBufferPassCallback (interfaz)**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Interfaz INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 