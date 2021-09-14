---
description: El método EffectSwapPriorities cambia los niveles de prioridad de dos efectos.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: Método IAMTimelineEffectable::EffectSwapPriorities (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887052"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>IamTimelineEffectable::EffectSwapPriorities (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `EffectSwapPriorities` método cambia los niveles de prioridad de dos efectos.

Dados dos valores de prioridad, este método intercambia los efectos en esas prioridades. Cuando el método vuelve, el efecto que estaba en el primer nivel de prioridad está en el segundo nivel de prioridad y viceversa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PrioridadA* 
</dt> <dd>

Primer nivel de prioridad en el que se intercambian los efectos.

</dd> <dt>

*PriorityB* 
</dt> <dd>

Segundo nivel de prioridad en el que intercambiar efectos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

[**IAMTimelineEffectable (interfaz)**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




