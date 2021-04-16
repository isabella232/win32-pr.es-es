---
description: El \_ método put mediatype establece el tipo de medio de salida en el filtro de tamaño.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize: método de ut_MediaType de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679456"
---
# <a name="iresizeput_mediatype-method"></a>IResize::p el \_ método UT mediatype

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_MediaType` método establece el tipo de medio de salida en el filtro de tamaño.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pago* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contiene el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

DES llama a este método antes de conectar el PIN de salida del filtro. Use el tipo de medio como el tipo de medio del terminal de salida. Devuelva este tipo de medio en el método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) y compruebe agsint este tipo en el método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) . DES nunca llama a este método después de que el PIN de salida esté conectado.

Actualmente, DES siempre establece el tipo de medio de salida en un formato RGB sin comprimir con un bloque de formato **VIDEOINFOHEADER** (el tipo de formato es igual a formato de \_ videoinfo). El subtipo podría ser MEDIASUBTYPE \_ ARGB32, que indica RGB de 32 bits con un canal alfa.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9,0 o posterior<br/>                                                         |
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**Interfaz IResize**](iresize.md)
</dt> </dl>

 

 




