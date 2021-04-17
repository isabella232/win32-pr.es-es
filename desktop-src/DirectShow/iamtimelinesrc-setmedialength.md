---
description: El método SetMediaLength especifica la duración del archivo de código fuente.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'IAMTimelineSrc:: SetMediaLength (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690937"
---
# <a name="iamtimelinesrcsetmedialength-method"></a>IAMTimelineSrc:: SetMediaLength (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetMediaLength` método especifica la duración del archivo de código fuente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Duración* 
</dt> <dd>

Longitud del medio, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Puede evitar posibles errores de representación si establece la longitud del medio antes de establecer la hora de detención del medio. Al establecer el tiempo de detención del medio, DES lo comprueba con la longitud del medio.

Este método no valida el parámetro de *longitud* , pero el valor debe ser igual a la duración real del archivo de código fuente. Obtenga la duración del archivo de origen mediante una llamada a [**IMediaDet:: get \_ StreamLength**](imediadet-get-streamlength.md).

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

[**Interfaz IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




