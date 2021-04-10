---
title: Método NOTIFY de IAMWMBufferPassCallback
description: El PIN llama al método Notify para cada búfer que se entrega durante el streaming.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Método Notify formato de Windows Media
- Método Notify formato de Windows Media, interfaz IAMWMBufferPassCallback
- Interfaz IAMWMBufferPassCallback formato de Windows Media, método Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149525"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>IAMWMBufferPassCallback:: NOTIFY (método)

El PIN llama al método **Notify** para cada búfer que se entrega durante el streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNSSBuffer3* \[ de\]
</dt> <dd>

Puntero a la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) expuesta en el ejemplo multimedia.

</dd> <dt>

*pPin* \[ de\]
</dt> <dd>

Puntero al pin asociado a la secuencia de medios a la que pertenece el ejemplo.

</dd> <dt>

*prtStart* \[ de\]
</dt> <dd>

Hora de inicio del ejemplo.

</dd> <dt>

*prtEnd* \[ de\]
</dt> <dd>

Hora de finalización del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se especifica ningún valor devuelto determinado. El PIN que realiza la llamada omite el **HRESULT**.

## <a name="remarks"></a>Observaciones

Este método permite que una aplicación examine y actúe sobre la información del búfer multimedia antes de que se procese el contenido del búfer. La aplicación es responsable de conocer el tipo de medio del PIN. Esta información se puede obtener obteniendo primero la información de la secuencia del perfil y, a continuación, llamando al método [**IConfigAsfWriter2:: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) para determinar qué PIN está asociado a cada flujo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de QASF de DirectShow**](directshow-qasf-reference.md)
</dt> <dt>

[**Interfaz IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Interfaz INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 