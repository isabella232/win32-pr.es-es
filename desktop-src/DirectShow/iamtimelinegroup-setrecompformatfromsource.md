---
description: El método SetRecompFormatFromSource establece el formato de recompresión de vídeo con el formato de compresión de un archivo de código fuente.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'IAMTimelineGroup:: SetRecompFormatFromSource (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680918"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>IAMTimelineGroup:: SetRecompFormatFromSource (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetRecompFormatFromSource` método establece el formato de recompresión de vídeo con el formato de compresión de un archivo de código fuente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSource* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineSrc**](iamtimelinesrc.md) del objeto de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                             | Descripción                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                                                                                    |
| <dl> <dt>**E \_ sin \_ escala de tiempo**</dt> </dl>          | El grupo no está dentro de una escala de tiempo.<br/>                                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memoria insuficiente.<br/>                                                                        |
| <dl> <dt>**\_puntero E**</dt> </dl>               | Argumento de puntero **nulo** .<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido. El grupo no es un grupo de vídeos o el archivo de origen no tiene ningún flujo de vídeo.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método busca el archivo de código fuente asociado a *pSource*, recupera el tipo de medio de la primera secuencia de vídeo en el archivo y establece el formato de compresión de grupo mediante ese tipo. Para obtener más información sobre los formatos de compresión, vea [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).

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

[**Interfaz IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




