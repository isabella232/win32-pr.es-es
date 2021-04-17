---
description: El método GetStartStop recupera las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'IAMTimelineObj:: GetStartStop (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690280"
---
# <a name="iamtimelineobjgetstartstop-method"></a>IAMTimelineObj:: GetStartStop (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetStartStop` método recupera las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStart* 
</dt> <dd>

Recibe la hora de inicio, en unidades de 100-nanosegundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recibe la hora de detención, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las composiciones, los grupos y las pistas siempre tienen una hora de inicio de 0.

Durante la representación, DES redondea las horas de inicio y detención de un objeto al límite de fotogramas más cercano. Sin embargo, DES no sobrescribe las horas del objeto. Si cambia la velocidad de fotogramas de grupo, los tiempos redondeados siempre se calculan a partir de las horas originales. Para obtener más información, [en servicios de edición de DirectShow](time-in-directshow-editing-services.md).

Para determinar las horas de inicio y detención en el proyecto representado, pase los valores devueltos por `GetStartStop` al método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) .

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

 

 




