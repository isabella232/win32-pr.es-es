---
description: El método \_ get FrameRate recupera la velocidad de fotogramas de la secuencia actual. La secuencia debe ser una secuencia de vídeo.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: Método IMediaDet::get_FrameRate (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886929"
---
# <a name="imediadetget_framerate-method"></a>IMediaDet::get \_ FrameRate (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_FrameRate` método recupera la velocidad de fotogramas de la secuencia actual. La secuencia debe ser una secuencia de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe la velocidad de fotogramas, en fotogramas por segundo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                             | Descripción                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | El encabezado de formato de vídeo no especifica una velocidad de fotogramas.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argumento no válido.<br/>                                  |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>               | **Argumento de** puntero NULL.<br/>                         |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                                |



 

## <a name="remarks"></a>Observaciones

Este método no puede recuperar la velocidad de fotogramas de un archivo ASF.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMediaDet (interfaz)**](imediadet.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




