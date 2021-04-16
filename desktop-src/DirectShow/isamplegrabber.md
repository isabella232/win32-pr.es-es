---
description: La interfaz ISampleGrabber se expone mediante el filtro de enganche de ejemplo. Permite que una aplicación recupere muestras de medios individuales a medida que se mueven por el gráfico de filtro.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interfaz ISampleGrabber (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678942"
---
# <a name="isamplegrabber-interface"></a>Interfaz ISampleGrabber

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La interfaz **ISampleGrabber** se expone mediante el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) . Permite que una aplicación recupere muestras de medios individuales a medida que se mueven por el gráfico de filtro.

## <a name="members"></a>Miembros

La interfaz **ISampleGrabber** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISampleGrabber** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISampleGrabber** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | Recupera el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | Recupera una copia del ejemplo que el filtro recibió más recientemente.<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | Sin implementar.<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | Especifica si se van a copiar los datos de ejemplo en un búfer a medida que pasa por el filtro.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Especifica un método de devolución de llamada al que llamar en los ejemplos de entrada.<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | Especifica el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | Especifica si el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) se detiene después de que el filtro reciba un ejemplo.<br/> |



 

## <a name="remarks"></a>Observaciones

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
</dt> </dl>

 

 
