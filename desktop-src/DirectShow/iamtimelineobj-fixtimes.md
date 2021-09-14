---
description: El método FixTimes redondea las horas de inicio y de detenerse especificadas a los límites de fotograma más cercanos, tal como se define en la configuración de velocidad de fotogramas del grupo primario.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: Método IAMTimelineObj::FixTimes (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892009"
---
# <a name="iamtimelineobjfixtimes-method"></a>IamTimelineObj::FixTimes (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método redondea las horas de inicio y de detenerse especificadas a los límites de fotogramas más cercanos, tal como se define en la configuración de velocidad de fotogramas del grupo `FixTimes` primario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio, en unidades de 100 nanosegundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que contiene la hora de detenerse, en unidades de 100 nanosegundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o E \_ NOTINTREE si el objeto no forma parte de un grupo.

## <a name="remarks"></a>Observaciones

Durante la representación, DES redondea las horas de inicio y de detenerse del objeto al límite de fotograma más cercano. Sin embargo, DES no sobrescribe las horas del objeto. Si cambia la velocidad de fotogramas del grupo, las horas redondeadas siempre se calculan a partir de las horas originales. Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Use este método para determinar las horas de inicio y de detenerse precisas en el proyecto representado. Por ejemplo, debe buscar las horas redondeadas, en lugar de las horas de inicio y de detenerse originales del objeto. Llame [**a IAMTimelineObj::GetStartStop para**](iamtimelineobj-getstartstop.md) obtener las horas originales y pase esos valores a `FixTimes` .

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




