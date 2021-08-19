---
description: El método EffectInsBefore inserta un efecto en el objeto en el nivel de prioridad especificado.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: Método IAMTimelineEffectable::EffectInsBefore (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0eca93a6c1837b8a7a8f5a95a6cdbf9e87f99191c0911a82e6fd7a3586eb8c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052755"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>IamTimelineEffectable::EffectInsBefore (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `EffectInsBefore` método inserta un efecto en el objeto en el nivel de prioridad especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pfx* 
</dt> <dd>

Puntero a la [**interfaz IAMTimelineObj**](iamtimelineobj.md) del efecto.

</dd> <dt>

*Prioridad* 
</dt> <dd>

Nivel de prioridad en el que se va a insertar el efecto. Use el valor –1 para insertar el efecto al final de la lista de prioridad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o E \_ NOTIMPL si el objeto no es un efecto. De lo contrario, devuelve **otro valor HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Las horas de inicio y de detenerse del efecto se recortan dentro de los límites del intervalo de tiempo del objeto, si es necesario. Si ya hay un efecto en el nivel de prioridad especificado, todos los efectos de ese punto se desplazan hacia abajo en la lista de prioridad para hacer espacio para el nuevo efecto.

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

[**IAMTimelineEffectable (interfaz)**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




