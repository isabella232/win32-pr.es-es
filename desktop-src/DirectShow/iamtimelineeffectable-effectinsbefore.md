---
description: El método EffectInsBefore inserta un efecto en el objeto en el nivel de prioridad especificado.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'IAMTimelineEffectable:: EffectInsBefore (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681255"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>IAMTimelineEffectable:: EffectInsBefore (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `EffectInsBefore` método inserta un efecto en el objeto en el nivel de prioridad especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFX* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del efecto.

</dd> <dt>

*Prioridad* 
</dt> <dd>

Nivel de prioridad en el que se va a insertar el efecto. Use el valor-1 para insertar el efecto al final de la lista de prioridades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si es correcto o E \_ NOTIMPL si el objeto no es un efecto. De lo contrario, devuelve otro valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Las horas de inicio y detención del efecto se recortan dentro de los límites del intervalo de tiempo del objeto, si es necesario. Si ya hay un efecto en el nivel de prioridad especificado, todos los efectos de ese punto en se mueven hacia abajo en la lista de prioridades para dejar espacio al nuevo efecto.

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

[**Interfaz IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




