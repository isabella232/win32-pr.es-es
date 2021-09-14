---
description: El método SetCallback especifica un método de devolución de llamada para llamar a en los ejemplos entrantes.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: Método ISampleGrabber::SetCallback (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891708"
---
# <a name="isamplegrabbersetcallback-method"></a>ISampleGrabber::SetCallback (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método SetCallback** especifica un método de devolución de llamada para llamar a en los ejemplos entrantes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCallback* 
</dt> <dd>

Puntero a una [**interfaz ISampleGrabberCB**](isamplegrabbercb.md) que contiene el método de devolución de llamada o **NULL** para cancelar la devolución de llamada.

</dd> <dt>

*WhichMethodToCallback* 
</dt> <dd>

Índice que especifica el método de devolución de llamada. Debe ser uno de los siguientes valores:



| Value | Descripción                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | El filtro Sample Grabber llama al [**método ISampleGrabberCB::SampleCB.**](isamplegrabbercb-samplecb.md) Este método recibe un [**puntero IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample)               |
| 1     | El filtro Sample Grabber llama al [**método ISampleGrabberCB::BufferCB.**](isamplegrabbercb-buffercb.md) Este método recibe un puntero al búfer contenido en el ejemplo multimedia. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El subproceso de procesamiento de datos se bloquea hasta que se devuelve el método de devolución de llamada. Si la devolución de llamada no se devuelve rápidamente, puede interferir con la reproducción.

El filtro no invoca la función de devolución de llamada para los ejemplos de inscripción previa ni para los ejemplos en los que el **miembro dwStreamId** de la estructura [**PROPERTIES DE AM \_ SAMPLE2 \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) no es otro que AM STREAM \_ \_ MEDIA.

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

 

 




