---
description: El método GetMediaTimes recupera las horas de inicio y detención del medio.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'IAMTimelineSrc:: GetMediaTimes (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690947"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a>IAMTimelineSrc:: GetMediaTimes (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetMediaTimes` método recupera las horas de inicio y detención del medio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStart* 
</dt> <dd>

Recibe la hora de inicio del medio, en unidades de 100 nanosegundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recibe la hora de detención del medio, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Los tiempos de los medios son relativos al archivo multimedia original. Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

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

 

 




