---
description: El método \_ get OutputStreams recupera el número de secuencias de audio y vídeo contenidas en el origen multimedia. Cualquier otro tipo de flujo, como los flujos de datos, se omite.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: Método IMediaDet::get_OutputStreams (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 19081afd1c005c61d39fc91cda8c28a93fface2a03b672411ef6449f75fa66fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083755"
---
# <a name="imediadetget_outputstreams-method"></a>Método IMediaDet::get \_ OutputStreams

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_OutputStreams` método recupera el número de secuencias de audio y vídeo contenidas en el origen multimedia. Cualquier otro tipo de flujo, como los flujos de datos, se omite.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe el número de flujos de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, llame a [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) para establecer el nombre de archivo. Si el detector de medios está en modo de captura de mapa de bits, este método devuelve E \_ INVALIDARG. Para obtener más información, [**vea IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




