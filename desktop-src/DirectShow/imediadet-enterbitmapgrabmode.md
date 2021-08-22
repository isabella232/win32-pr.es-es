---
description: El método EnterBitmapGrabMode cambia el detector de medios al modo de captura de mapa de bits y busca el gráfico de filtro a una hora especificada.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: Método IMediaDet::EnterBitmapGrabMode (Qedit.h)
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
ms.openlocfilehash: d47989b95663a9a99f4363fb505aec996ea23acdd813cf301f7ee252c874dc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952624"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>Método IMediaDet::EnterBitmapGrabMode

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método cambia el detector de medios al modo de captura de mapa de bits y busca el `EnterBitmapGrabMode` gráfico de filtro a una hora especificada.

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

Tiempo, en segundos, al que busca el gráfico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                             | Descripción                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argumento no válido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | El archivo de origen no tiene una secuencia de vídeo.<br/> |
| <dl> <dt>**TIEMPO DE VFW \_ E \_ \_ EXPIRADO**</dt> </dl>    | Se ha pasado el tiempo de espera del comando Seek.<br/>                       |



 

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, establezca el nombre de archivo y la secuencia llamando a [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Este método inserta el filtro [**Sample Grabber**](sample-grabber-filter.md) en el gráfico de filtros. A continuación, puede llamar a [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) para obtener un puntero a la [**interfaz ISampleGrabber.**](isamplegrabber.md) Una vez que el detector de medios entra en modo de captura de mapa de bits, los distintos métodos informativos **de IMediaDet** no funcionan.

Los [**métodos IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) también ponen el detector de medios en modo de captura de mapa de bits.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaDet (interfaz)**](imediadet.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




