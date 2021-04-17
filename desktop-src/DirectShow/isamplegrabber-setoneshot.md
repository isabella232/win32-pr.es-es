---
description: El método SetOneShot especifica si el filtro de enganche de ejemplo se detiene después de que el filtro reciba un ejemplo.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'ISampleGrabber:: SetOneShot (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679507"
---
# <a name="isamplegrabbersetoneshot-method"></a>ISampleGrabber:: SetOneShot (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método **SetOneShot** especifica si el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) se detiene después de que el filtro reciba un ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OneShot* 
</dt> <dd>

Valor booleano que especifica si el filtro de enganche de ejemplo se detiene tras recibir un ejemplo.



| Value                                                                                                                                    | Significado                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | El enganche de ejemplo se detiene después del primer ejemplo. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Después del primer ejemplo, el enganche de ejemplo continúa procesando ejemplos. Este es el comportamiento predeterminado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Use este método para obtener una muestra única de la secuencia, como se indica a continuación:

1.  Llame a **SetOneShot** con el valor **true**.
2.  Opcionalmente, use la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) para buscar una posición en la secuencia.
3.  Llame a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico de filtro.
4.  Llame a [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) para esperar a que el gráfico se detenga. Como alternativa, llame a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obtener eventos de gráfico, hasta que reciba el evento de [**\_ finalización de EC**](ec-complete.md) .

Una vez que se detiene el enganche de ejemplo, el gráfico de filtro sigue en estado en ejecución. Puede buscar o pausar el gráfico para obtener otro ejemplo.

> [!Note]  
> Una versión anterior de la documentación indicó que el gráfico de filtro se detiene una vez recibido el ejemplo. Eso no es preciso. La secuencia finaliza, pero el gráfico permanece en el estado en ejecución.

 

El enganche de ejemplo implementa el modo de una sola toma llamando a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el filtro de nivel inferior y devuelve S \_ false desde el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

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

 

 




