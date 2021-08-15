---
description: El método BufferCB es un método de devolución de llamada que recibe un puntero al búfer de ejemplo.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: Método ISampleGrabberCB::BufferCB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c92e83c8daf5bf129a9aa8330bcc53caa88537f2395aeceebd8b5da2037c5b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817595"
---
# <a name="isamplegrabbercbbuffercb-method"></a>ISampleGrabberCB::BufferCB (Método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El **método BufferCB** es un método de devolución de llamada que recibe un puntero al búfer de ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SampleTime* 
</dt> <dd>

Hora de inicio de la muestra, en segundos.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntero a un búfer que contiene los datos de ejemplo. El formato de los datos depende del tipo de medio del pin de entrada de Sample Grabber. Para obtener el tipo de medio, llame [**a ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).

</dd> <dt>

*BufferLen* 
</dt> <dd>

Longitud del búfer al que apunta *pBuffer*, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un código de error **HRESULT** en caso contrario.

## <a name="remarks"></a>Comentarios

Este método de devolución de llamada recibe un puntero a los datos del ejemplo multimedia más reciente.

> [!Note]  
> Este método recibe un puntero a los datos de ejemplo originales, no una copia. La documentación original indicaba incorrectamente que *pBuffer* contiene una copia de los datos.

 

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

 

 




