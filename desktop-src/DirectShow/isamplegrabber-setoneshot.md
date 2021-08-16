---
description: El método SetOneShot especifica si el filtro Sample Grabber se detiene después de que el filtro recibe una muestra.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: Método ISampleGrabber::SetOneShot (Qedit.h)
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
ms.openlocfilehash: 7829bd57cb2d813f71e17a4925d6e5fab7cc34330041461b691e00eae6ca5cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817686"
---
# <a name="isamplegrabbersetoneshot-method"></a>ISampleGrabber::SetOneShot (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método SetOneShot** especifica si el filtro [**Sample Grabber**](sample-grabber-filter.md) se detiene después de que el filtro recibe una muestra.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Oneshot* 
</dt> <dd>

Valor booleano que especifica si el filtro Sample Grabber se detiene después de recibir una muestra.



| Valor                                                                                                                                    | Significado                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE**</dt> </dl>    | Sample Grabber se detiene después del primer ejemplo. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE**</dt> </dl> | Después del primer ejemplo, sample Grabber continúa procesando muestras. Este es el comportamiento predeterminado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Use este método para obtener un solo ejemplo de la secuencia, como se muestra a continuación:

1.  Llame **a SetOneShot** con el **valor TRUE.**
2.  Opcionalmente, use la [**interfaz IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) para buscar una posición en la secuencia.
3.  Llame [**a IMediaControl::Run para**](/windows/desktop/api/Control/nf-control-imediacontrol-run) ejecutar el gráfico de filtro.
4.  Llame [**a IMediaEvent::WaitForCompletion para**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) esperar a que se detenga el gráfico. Como alternativa, llame [**a IMediaEvent::GetEvent para**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) obtener eventos de grafo, hasta que reciba el [**evento EC \_ COMPLETE.**](ec-complete.md)

Después de que se detenga Sample Grabber, el gráfico de filtro sigue en estado en ejecución. Puede buscar o pausar el gráfico para obtener otro ejemplo.

> [!Note]  
> Una versión anterior de la documentación indicaba que el gráfico de filtros se detiene después de recibir el ejemplo. Eso no es preciso. La secuencia finaliza, pero el gráfico permanece en estado en ejecución.

 

Sample Grabber implementa el modo de una sola toma llamando a [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el filtro de bajada y devolviendo S FALSE desde el método \_ [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de él.

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

 

 




