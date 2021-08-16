---
description: El método SampleCB es un método de devolución de llamada que recibe un puntero al ejemplo multimedia.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: Método ISampleGrabberCB::SampleCB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e98377050ec98cdccaedd54119afb6cdaccbaee56256f1406bb190d3ea875bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817517"
---
# <a name="isamplegrabbercbsamplecb-method"></a>ISampleGrabberCB::SampleCB (Método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SampleCB` método es un método de devolución de llamada que recibe un puntero al ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SampleTime* 
</dt> <dd>

Hora de inicio de la muestra, en segundos.

</dd> <dt>

*pSample* 
</dt> <dd>

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un código de error **HRESULT** en caso contrario.

## <a name="remarks"></a>Comentarios

Para configurar la devolución de llamada, llame [**a ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).

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

[Códigos de error y correcto](error-and-success-codes.md)
</dt> <dt>

[**Interfaz ISampleGrabberCB**](isamplegrabbercb.md)
</dt> </dl>

 

 




