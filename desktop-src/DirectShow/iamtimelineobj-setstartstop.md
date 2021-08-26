---
description: El método SetStartStop establece las horas de inicio y de detenerse del objeto, en relación con el elemento primario del objeto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: Método IAMTimelineObj::SetStartStop (Qedit.h)
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
ms.openlocfilehash: e2806d926c9842f5900f46f923f4cbdf8caa47f112e1832077ab7d2b80a9341c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052455"
---
# <a name="iamtimelineobjsetstartstop-method"></a>IamTimelineObj::SetStartStop (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetStartStop` método establece las horas de inicio y de detenerse del objeto, en relación con el elemento primario del objeto.

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

Nueva hora de inicio, en unidades de 100 nanosegundos, o –1 para mantener la hora de inicio existente.

</dd> <dt>

*Detención* 
</dt> <dd>

Nueva hora de detenerse, en unidades de 100 nanosegundos, o –1 para mantener la hora de detenerse existente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                  | Descripción                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Sin implementar.<br/>  |



 

## <a name="remarks"></a>Comentarios

Las pistas, las composiciones y los grupos no implementan este método. Para estos objetos, la hora de inicio siempre es cero y la hora de detención es el tiempo de detención máximo de los objetos que contienen.

No establezca horas superpuestas en objetos de origen dentro de la misma pista. Esto puede provocar comportamientos indefinidos.

En el caso de los objetos de origen, las horas de inicio y de detenerse son independientes de las horas de inicio y de detención de medios. Cambiar un par de valores no cambia el otro. Para establecer las horas de inicio y de detenerse de los medios, llame al [**método IAMTimelineSrc::SetMediaTimes.**](iamtimelinesrc-setmediatimes.md) Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Para obtener cortes y transiciones precisos del marco, establezca los parámetros *Start* y *Stop* en límites de marco. Puede usar el [**método IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) para convertir un valor de tiempo en el límite de marco más cercano, o bien usar la siguiente función para convertir el número de fotograma a la hora de referencia:


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

[**IAMTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




