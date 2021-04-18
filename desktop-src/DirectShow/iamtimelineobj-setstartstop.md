---
description: El método SetStartStop establece las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'IAMTimelineObj:: SetStartStop (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690721"
---
# <a name="iamtimelineobjsetstartstop-method"></a>IAMTimelineObj:: SetStartStop (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetStartStop` método establece las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Nueva hora de inicio, en unidades de 100-nanosegundos, o – 1 para mantener la hora de inicio existente.

</dd> <dt>

*Detención* 
</dt> <dd>

Nueva hora de detención, en unidades de 100-nanosegundos, o – 1 para mantener la hora de detención existente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                  | Descripción                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Sin implementar.<br/>  |



 

## <a name="remarks"></a>Observaciones

Las pistas, las composiciones y los grupos no implementan este método. Para estos objetos, la hora de inicio siempre es cero y la hora de detención es el tiempo de detención máximo de los objetos que contienen.

No establezca tiempos de superposición en objetos de origen dentro de la misma pista. Si lo hace, pueden producirse comportamientos indefinidos.

En el caso de los objetos de origen, los tiempos de inicio y detención son independientes de los tiempos de inicio y detención del medio. Al cambiar un par de valores, no se cambia el otro. Para establecer las horas de inicio y detención del medio, llame al método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Para obtener cortes y transiciones con precisión de fotogramas, establezca los parámetros de *Inicio* y *detención* en los límites del marco. Puede usar el método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) para convertir un valor de hora en el límite de fotograma más cercano, o bien usar la función siguiente para convertir de número de fotograma a hora de referencia:


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



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

 

 




