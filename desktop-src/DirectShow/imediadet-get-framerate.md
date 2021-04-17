---
description: El \_ método get de velocidad de fotogramas recupera la velocidad de fotogramas de la secuencia actual. La secuencia debe ser una secuencia de vídeo.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Método IMediaDet:: get_FrameRate (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680895"
---
# <a name="imediadetget_framerate-method"></a>IMediaDet:: get \_ velocidad (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_FrameRate` método recupera la velocidad de fotogramas de la secuencia actual. La secuencia debe ser una secuencia de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Recibe la velocidad de fotogramas, en fotogramas por segundo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                             | Descripción                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                 | El encabezado de formato de vídeo no especifica una velocidad de fotogramas.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argumento no válido.<br/>                                  |
| <dl> <dt>**\_puntero E**</dt> </dl>               | Argumento de puntero **nulo** .<br/>                         |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                                |



 

## <a name="remarks"></a>Observaciones

Este método no puede recuperar la velocidad de fotogramas de un archivo ASF.

Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG. Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




