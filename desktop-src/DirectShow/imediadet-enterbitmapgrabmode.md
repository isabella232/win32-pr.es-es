---
description: El método EnterBitmapGrabMode cambia el detector de medios al modo de agarre de mapa de bits y busca el gráfico de filtro en un tiempo especificado.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'IMediaDet:: EnterBitmapGrabMode (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680231"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>IMediaDet:: EnterBitmapGrabMode (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `EnterBitmapGrabMode` método cambia el detector de medios por el modo de captura de mapa de bits y busca el gráfico de filtro en un tiempo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StreamTime* 
</dt> <dd>

Tiempo, en segundos, que busca el gráfico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                             | Descripción                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argumento no válido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | El archivo de origen no tiene una secuencia de vídeo.<br/> |
| <dl> <dt>**\_ \_ expiró el tiempo de VFW E \_**</dt> </dl>    | Se agotó el tiempo de espera del comando de búsqueda.<br/>                       |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Este método inserta el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) en el gráfico de filtro. Después, puede llamar a [**IMediaDet:: GetSampleGrabber**](imediadet-getsamplegrabber.md) para obtener un puntero a la interfaz [**ISampleGrabber**](isamplegrabber.md) . Una vez que el detector de medios entra en el modo de captura de mapas de bits, los distintos métodos informativos de **IMediaDet** no funcionan.

Los métodos [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md) también colocan el detector de medios en el modo de agarre de mapa de bits.

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

 

 




