---
description: El método GetCurrentBuffer recupera una copia del búfer asociado al ejemplo más reciente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'ISampleGrabber:: GetCurrentBuffer (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680643"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>ISampleGrabber:: GetCurrentBuffer (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método **GetCurrentBuffer** recupera una copia del búfer asociado al ejemplo más reciente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBufferSize* \[ in, out\]
</dt> <dd>

Puntero al tamaño del búfer. Si *pBuffer* es **null**, este parámetro recibe el tamaño de búfer necesario, en bytes. Si *pBuffer* no es **null**, establezca este parámetro igual al tamaño del búfer, en bytes. En la salida, el parámetro recibe el número de bytes que se copiaron en el búfer. Este valor puede ser menor que el tamaño del búfer.

</dd> <dt>

*pBuffer* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de bytes de tamaño *pBufferSize* o **null**. Si este parámetro no es **null**, el búfer actual se copia en la matriz. Si este parámetro es **null**, el parámetro *pBufferSize* recibe el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                           | Descripción                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Los ejemplos no se almacenan en búfer. Llame a [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md).<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | El búfer especificado no es suficientemente grande.<br/>                                                                         |
| <dl> <dt>**\_puntero E**</dt> </dl>             | Argumento de puntero **nulo** .<br/>                                                                                        |
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El filtro no está conectado.<br/>                                                                                      |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl>   | El filtro no ha recibido todavía ningún ejemplo. Para ofrecer un ejemplo, ejecute o Pause el gráfico.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Para activar el almacenamiento en búfer, llame a [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con un valor de **true**.

Llame a este método dos veces. En la primera llamada, establezca *pBuffer* en **null**. El tamaño del búfer se devuelve en *pBufferSize*. A continuación, asigne una matriz y llame de nuevo al método. En la segunda llamada, se pasa el tamaño de la matriz en *pBufferSize* y se pasa la dirección de la matriz en *pBuffer*. Si la matriz no es suficientemente grande, el método devuelve E \_ OUTOFMEMORY.

El parámetro *pBuffer* se escribe como un puntero **largo** , pero el contenido del búfer depende del formato de los datos. Llame a [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) para obtener el tipo de medio del formato.

No llame a este método mientras se está ejecutando el gráfico de filtro. Mientras se ejecuta el gráfico de filtros, el filtro de enganche de ejemplo sobrescribe el contenido del búfer cada vez que recibe un nuevo ejemplo. La mejor manera de utilizar este método es usar el "modo de una sola vacuna", que detiene el gráfico después de recibir el primer ejemplo. Para establecer el modo de una sola toma, llame a [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md).

El filtro no almacena en búfer ejemplos de prefijo, o muestras en las que el miembro **dwStreamId** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) es distinto de los \_ medios de secuencia AM \_ .

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

 

 




