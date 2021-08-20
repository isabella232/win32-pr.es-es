---
description: El método put \_ MediaType establece el tipo de medio de salida en el filtro de cambio de tamaño.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: Método IResize::p ut_MediaType (Qedit.h)
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
ms.openlocfilehash: 6c26878af6f091efd3c3f321cb073ce51a8e6236d4bafa326ab99f85f39e1a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818206"
---
# <a name="iresizeput_mediatype-method"></a>IResize::p ut \_ MediaType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_MediaType` método establece el tipo de medio de salida en el filtro de cambio de tamaño.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmt* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contiene el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

DES llama a este método antes de conectar el pin de salida del filtro. Use el tipo de medio como tipo de medio del pin de salida. Devuelve este tipo de medio en el método [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) y comprueba agsint este tipo en el [**método CTransformFilter::CheckTransform.**](ctransformfilter-checktransform.md) DES nunca llama a este método una vez conectado el pin de salida.

Actualmente, DES siempre establece el tipo de medio de salida en un formato RGB sin comprimir con un bloque de **formato VIDEOINFOHEADER** (el tipo de formato es igual a FORMAT \_ VideoInfo). El subtipo podría ser MEDIASUBTYPE \_ ARGB32, que indica RGB de 32 bits con un canal alfa.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9.0 o posterior<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**IResize (Interfaz)**](iresize.md)
</dt> </dl>

 

 




