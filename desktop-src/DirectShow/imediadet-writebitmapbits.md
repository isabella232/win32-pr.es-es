---
description: El método WriteBitmapBits recupera un fotograma de vídeo en el tiempo medio especificado y lo escribe en un archivo. El fotograma de vídeo siempre tiene el formato RGB de 24 bits.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'IMediaDet:: WriteBitmapBits (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679531"
---
# <a name="imediadetwritebitmapbits-method"></a>IMediaDet:: WriteBitmapBits (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `WriteBitmapBits` método recupera un fotograma de vídeo en el tiempo medio especificado y lo escribe en un archivo. El fotograma de vídeo siempre tiene el formato RGB de 24 bits.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StreamTime* 
</dt> <dd>

Hora a la que se va a recuperar el fotograma de vídeo.

</dd> <dt>

*Width* 
</dt> <dd>

Ancho de la imagen, en píxeles.

</dd> <dt>

*Height* 
</dt> <dd>

Alto de la imagen, en píxeles.

</dd> <dt>

*Nombre de archivo* 
</dt> <dd>

Ruta de acceso del archivo en el que se va a guardar el mapa de bits. Si el archivo ya existe, este método lo sobrescribe.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S correcto \_ . De lo contrario, devuelve un valor **HRESULT** que indica la causa del error. Entre los posibles códigos de error se incluyen los siguientes:



| Código devuelto                                                                                             | Descripción                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOinterface**</dt> </dl>           | No se pudo agregar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) al gráfico.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                  | Error.<br/>                                                                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memoria insuficiente.<br/>                                                                   |
| <dl> <dt>**E \_ inesperado**</dt> </dl>            | error inesperado.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ ACCESSDENIED**</dt> </dl>     | No se puede sobrescribir el archivo.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                                                                    |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Este método coloca el detector de medios en el modo de agarre de mapa de bits. Una vez que se ha llamado a este método, los distintos métodos de información de secuencia de **IMediaDet** no funcionan, a menos que cree una nueva instancia del detector de medios.

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

 

 




