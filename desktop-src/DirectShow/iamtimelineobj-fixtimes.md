---
description: El método FixTimes redondea las horas de inicio y detención especificadas a los límites del marco más cercano, según se define en la configuración de velocidad de fotogramas del grupo primario.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'IAMTimelineObj:: FixTimes (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691061"
---
# <a name="iamtimelineobjfixtimes-method"></a>IAMTimelineObj:: FixTimes (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `FixTimes` método redondea las horas de inicio y detención especificadas a los límites del marco más cercano, según se define en la configuración de velocidad de fotogramas del grupo primario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FixTimes(
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

Devuelve \_ si es correcto, o E \_ NOTINTREE si el objeto no forma parte de un grupo.

## <a name="remarks"></a>Observaciones

Durante la representación, DES redondea las horas de inicio y detención del objeto al límite de fotogramas más cercano. Sin embargo, DES no sobrescribe las horas del objeto. Si cambia la velocidad de fotogramas de grupo, los tiempos redondeados siempre se calculan a partir de las horas originales. Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Use este método para determinar los tiempos de inicio y detención precisos en el proyecto representado. Por ejemplo, debe buscar las horas redondeadas, en lugar de las horas de inicio y detención originales del objeto. Llame a [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md) para obtener las horas originales y pase esos valores a `FixTimes` .

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

[**Interfaz IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




