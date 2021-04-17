---
description: El método SampleCB es un método de devolución de llamada que recibe un puntero al ejemplo multimedia.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'ISampleGrabberCB:: SampleCB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680961"
---
# <a name="isamplegrabbercbsamplecb-method"></a>ISampleGrabberCB:: SampleCB (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SampleCB` método es un método de devolución de llamada que recibe un puntero al ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SampleTime* 
</dt> <dd>

Hora de inicio del ejemplo, en segundos.

</dd> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente o un código de error **HRESULT** en caso contrario.

## <a name="remarks"></a>Observaciones

Para configurar la devolución de llamada, llame a [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).

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

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**Interfaz ISampleGrabberCB**](isamplegrabbercb.md)
</dt> </dl>

 

 




