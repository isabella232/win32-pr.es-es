---
description: El método VTrackSwapPriorities cambia los niveles de prioridad de dos pistas.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'IAMTimelineComp:: VTrackSwapPriorities (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691082"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>IAMTimelineComp:: VTrackSwapPriorities (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `VTrackSwapPriorities` método cambia los niveles de prioridad de dos pistas.

Dado dos niveles de prioridad, este método cambia las pistas virtuales en esas prioridades. Cuando el método devuelve, la pista que estaba en el primer nivel de prioridad ahora está en el segundo nivel de prioridad y viceversa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VirtualTrackA* 
</dt> <dd>

Primer nivel de prioridad en el que se van a intercambiar las pistas virtuales.

</dd> <dt>

*VirtualTrackB* 
</dt> <dd>

Segundo nivel de prioridad en el que se van a intercambiar las pistas virtuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

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

[**Interfaz IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




