---
description: El método SetBufferSamples especifica si se deben copiar los datos de ejemplo en un búfer a medida que pasa por el filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'ISampleGrabber:: SetBufferSamples (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680640"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>ISampleGrabber:: SetBufferSamples (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método **SetBufferSamples** especifica si se deben copiar los datos de ejemplo en un búfer a medida que pasa por el filtro.

## <a name="syntax"></a>Sintaxis


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BufferThem* 
</dt> <dd>

Valor booleano que especifica si se deben almacenar en búfer los datos de ejemplo. Si **es true**, el filtro copia los datos de ejemplo en un búfer interno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para obtener el búfer copiado, llame a [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).

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

 

 




