---
description: El método SetCallback especifica un método de devolución de llamada al que llamar en los ejemplos de entrada.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'ISampleGrabber:: SetCallback (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680641"
---
# <a name="isamplegrabbersetcallback-method"></a>ISampleGrabber:: SetCallback (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método **SetCallback** especifica un método de devolución de llamada al que llamar en los ejemplos de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCallback* 
</dt> <dd>

Puntero a una interfaz [**ISampleGrabberCB**](isamplegrabbercb.md) que contiene el método de devolución de llamada o **null** para cancelar la devolución de llamada.

</dd> <dt>

*WhichMethodToCallback* 
</dt> <dd>

Índice que especifica el método de devolución de llamada. Debe ser uno de los valores siguientes.



| Value | Descripción                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | El filtro de enganche de ejemplo llama al método [**ISampleGrabberCB:: SampleCB**](isamplegrabbercb-samplecb.md) . Este método recibe un puntero [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .               |
| 1     | El filtro de enganche de ejemplo llama al método [**ISampleGrabberCB:: BufferCB**](isamplegrabbercb-buffercb.md) . Este método recibe un puntero al búfer incluido en el ejemplo multimedia. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El subproceso de procesamiento de datos se bloquea hasta que se devuelve el método de devolución de llamada. Si la devolución de llamada no vuelve rápidamente, puede interferir con la reproducción.

El filtro no invoca la función de devolución de llamada para los ejemplos de prefijo o para los ejemplos en los que el miembro **dwStreamId** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) es distinto de la \_ secuencia de multimedia AM \_ .

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar el enganche de ejemplo](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaz ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




