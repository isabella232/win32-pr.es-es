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
ms.openlocfilehash: 6e79f3f83422290600b4b6e75dbf15daff161f5e913a0300645254cdf94e7c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928235"
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

Segundo nivel de prioridad en el que se intercambian los efectos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

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

[**IAMTimelineEffectable (Interfaz)**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




