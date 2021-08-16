---
description: El método SetBufferSamples especifica si se copian los datos de ejemplo en un búfer a medida que se pasa por el filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: Método ISampleGrabber::SetBufferSamples (Qedit.h)
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
ms.openlocfilehash: c768a21d4e08e6900f3a46f3e398f5040aaf6b6b0bc45c9187ac07821500a372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818000"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>ISampleGrabber::SetBufferSamples (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método SetBufferSamples** especifica si se copian los datos de ejemplo en un búfer a medida que se pasa por el filtro.

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

Valor booleano que especifica si se deben almacenar en búfer los datos de ejemplo. Si **es TRUE,** el filtro copia los datos de ejemplo en un búfer interno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para obtener el búfer copiado, llame a [**ISampleGrabber::GetCurrentBuffer.**](isamplegrabber-getcurrentbuffer.md)

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

 

 




