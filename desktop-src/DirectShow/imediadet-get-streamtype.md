---
description: El \_ método get StreamType recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Método IMediaDet:: get_StreamType (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690837"
---
# <a name="imediadetget_streamtype-method"></a>IMediaDet:: get \_ StreamType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_StreamType` método recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Recibe el GUID de tipo principal para el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método recupera el miembro **majortype** de la estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . La estructura de **\_ \_ tipo de medio am** describe el formato de la secuencia y el miembro **majortype** es un GUID que indica la categoría general, como audio o vídeo. En el caso de una secuencia de vídeo, el GUID es el vídeo de MEDIATYPE \_ . En el caso de audio, es de \_ audio MEDIATYPE. Para recuperar toda la estructura de **\_ \_ tipo de medio am** , llame al método [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md) .

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

 

 




