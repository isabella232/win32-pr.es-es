---
description: El método GetSampleGrabber recupera un puntero a la interfaz ISampleGrabber, lo que permite a una aplicación recuperar muestras individuales de un flujo multimedia.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: Método IMediaDet::GetSampleGrabber (Qedit.h)
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
ms.openlocfilehash: f2c3c580a44b9cff35d7ee801cfc611b5cf8a8df828f54c28b022e5c1a1b862a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819047"
---
# <a name="imediadetgetsamplegrabber-method"></a>IMediaDet::GetSampleGrabber (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetSampleGrabber` método recupera un puntero a la interfaz [**ISampleGrabber,**](isamplegrabber.md) que permite a una aplicación recuperar muestras individuales de un flujo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVal* \[ out\]
</dt> <dd>

Recibe un puntero a la [**interfaz ISampleGrabber.**](isamplegrabber.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Llame [**a IMediaDet::EnterBitmapGrabMode antes**](imediadet-enterbitmapgrabmode.md) de llamar a este método. La [**interfaz ISampleGrabber**](isamplegrabber.md) permite recuperar muestras de medios individuales de la secuencia. Si solo necesita un mapa de bits de un fotograma de vídeo, llame al método [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) en su lugar. La **interfaz ISampleGrabber** es más flexible, pero requiere más trabajo por parte de la aplicación.

Si este método se realiza correctamente, la [**interfaz ISampleGrabber**](isamplegrabber.md) que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMediaDet (interfaz)**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




