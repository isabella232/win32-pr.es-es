---
description: El método EffectSwapPriorities cambia los niveles de prioridad de dos efectos.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'IAMTimelineEffectable:: EffectSwapPriorities (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691078"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>IAMTimelineEffectable:: EffectSwapPriorities (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `EffectSwapPriorities` método cambia los niveles de prioridad de dos efectos.

Dados dos valores de prioridad, este método intercambia los efectos en esas prioridades. Cuando el método devuelve un resultado, el efecto que tenía en el primer nivel de prioridad está en el segundo nivel de prioridad y viceversa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Prioridada* 
</dt> <dd>

Primer nivel de prioridad en el que se intercambian los efectos.

</dd> <dt>

*PriorityB* 
</dt> <dd>

Segundo nivel de prioridad en el que se intercambian los efectos.

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

[**Interfaz IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




