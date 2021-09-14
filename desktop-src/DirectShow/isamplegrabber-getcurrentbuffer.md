---
description: El método GetCurrentBuffer recupera una copia del búfer asociado al ejemplo más reciente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: Método ISampleGrabber::GetCurrentBuffer (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891737"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>ISampleGrabber::GetCurrentBuffer (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método GetCurrentBuffer** recupera una copia del búfer asociado al ejemplo más reciente.

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

Puntero al tamaño del búfer. Si *pBuffer* es **NULL,** este parámetro recibe el tamaño de búfer necesario, en bytes. Si *pBuffer* no es **NULL,** establezca este parámetro igual al tamaño del búfer, en bytes. En la salida, el parámetro recibe el número de bytes que se copiaron en el búfer. Este valor puede ser menor que el tamaño del búfer.

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Puntero a una matriz de bytes de tamaño *pBufferSize* o **NULL.** Si este parámetro no es **NULL,** el búfer actual se copia en la matriz. Si este parámetro es **NULL,** el *parámetro pBufferSize* recibe el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                           | Descripción                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Los ejemplos no se están almacenando en búfer. Llame [**a ISampleGrabber::SetBufferSamples.**](isamplegrabber-setbuffersamples.md)<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | El búfer especificado no es lo suficientemente grande.<br/>                                                                         |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>             | **Argumento de** puntero NULL.<br/>                                                                                        |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El filtro no está conectado.<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt> </dl>   | El filtro aún no ha recibido ninguna muestra. Para entregar un ejemplo, ejecute o pause el gráfico.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Para activar el almacenamiento en búfer, llame a [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con un valor de **TRUE.**

Llame a este método dos veces. En la primera llamada, establezca *pBuffer* en **NULL.** El tamaño del búfer se devuelve en *pBufferSize*. A continuación, asigne una matriz y llame al método de nuevo. En la segunda llamada, pase el tamaño de la matriz en *pBufferSize* y pase la dirección de la matriz en *pBuffer*. Si la matriz no es lo suficientemente grande, el método devuelve E \_ OUTOFMEMORY.

El *parámetro pBuffer* se escribe como un **puntero** largo, pero el contenido del búfer depende del formato de los datos. Llame [**a ISampleGrabber::GetConnectedMediaType para**](isamplegrabber-getconnectedmediatype.md) obtener el tipo de medio del formato.

No llame a este método mientras se ejecuta el gráfico de filtros. Mientras se ejecuta el gráfico de filtros, el filtro Sample Grabber sobrescribe el contenido del búfer cada vez que recibe un nuevo ejemplo. La mejor manera de usar este método es usar el "modo de una sola toma", que detiene el gráfico después de recibir la primera muestra. Para establecer el modo de una sola toma, llame [**a ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).

El filtro no almacena en búfer ejemplos de inscripción previa, ni ejemplos en los que el **miembro dwStreamId** de la estructura DE PROPIEDADES [**DE AM \_ SAMPLE2 \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) sea distinto de AM STREAM \_ \_ MEDIA.

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

[Uso de Sample Grabber](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber (interfaz)**](isamplegrabber.md)
</dt> </dl>

 

 




