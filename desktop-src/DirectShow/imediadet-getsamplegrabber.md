---
description: El método GetSampleGrabber recupera un puntero a la interfaz ISampleGrabber, que permite que una aplicación recupere muestras individuales de una secuencia multimedia.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'IMediaDet:: GetSampleGrabber (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679535"
---
# <a name="imediadetgetsamplegrabber-method"></a>IMediaDet:: GetSampleGrabber (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetSampleGrabber` método recupera un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) , que permite que una aplicación recupere muestras individuales de una secuencia multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVal* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Llame a [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) antes de llamar a este método. La interfaz [**ISampleGrabber**](isamplegrabber.md) permite recuperar muestras de medios individuales de la secuencia. Si solo necesita un mapa de bits de un fotograma de vídeo, llame al método [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) en su lugar. La interfaz **ISampleGrabber** es más flexible, pero requiere más trabajo por parte de la aplicación.

Si este método se ejecuta correctamente, la interfaz [**ISampleGrabber**](isamplegrabber.md) que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

[**Interfaz IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




