---
description: El método FixMediaTimes redondea los valores de hora especificados al límite de fotogramas más cercano, según se define en la velocidad de fotogramas de salida. En general, las aplicaciones no necesitan llamar a este método.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'IAMTimelineSrc:: FixMediaTimes (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689967"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>IAMTimelineSrc:: FixMediaTimes (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `FixMediaTimes` método redondea los valores de hora especificados al límite de fotogramas más cercano, según se define en la velocidad de fotogramas de salida. En general, las aplicaciones no necesitan llamar a este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStart* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio, en unidades de 100-nanosegundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que contiene la hora de detención, en unidades de 100-nanosegundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método es similar al método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) , pero conserva la relación original de las horas de los medios y los tiempos de la escala de tiempo. Simplemente redondear las horas al límite de fotogramas más cercano podría distorsionar esta relación.

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

 

 




