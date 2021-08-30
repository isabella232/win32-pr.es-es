---
description: El método get \_ StreamType recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: Método IMediaDet::get_StreamType (Qedit.h)
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
ms.openlocfilehash: 1a027059854ba02e4a846660435731f140b6d04cb8d96f714fd63f1d24757ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083725"
---
# <a name="imediadetget_streamtype-method"></a>IMediaDet::get \_ StreamType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_StreamType` método recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe el GUID de tipo principal para el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método recupera el miembro **majortype** de la [**estructura AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) La **estructura AM MEDIA \_ \_ TYPE** describe el formato de la secuencia y el **miembro majortype** es un GUID que indica la categoría general, como audio o vídeo. Para una secuencia de vídeo, el GUID es MEDIATYPE \_ Video. En el caso del audio, es MEDIATYPE \_ Audio. Para recuperar toda la **estructura \_ AM MEDIA \_ TYPE,** llame al [**método IMediaDet::get \_ StreamMediaType.**](imediadet-get-streammediatype.md)

Antes de llamar a este método, establezca el nombre de archivo y la secuencia llamando a [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Si el detector de medios está en modo de captura de mapa de bits, este método devuelve E \_ INVALIDARG. Para obtener más información, [**vea IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




