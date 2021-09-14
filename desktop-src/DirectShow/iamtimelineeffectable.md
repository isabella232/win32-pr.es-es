---
description: La interfaz IAMTimelineEffectable proporciona métodos para agregar efectos a un objeto de escala de tiempo en DirectShow Editing Services (DES) y para manipular los efectos en un objeto.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interfaz IAMTimelineEffectable (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887033"
---
# <a name="iamtimelineeffectable-interface"></a>IamTimelineEffectable (interfaz)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La interfaz proporciona métodos para agregar efectos a un objeto de escala de tiempo `IAMTimelineEffectable` en DirectShow Editing [Services](directshow-editing-services.md) (DES) y para manipular los efectos en un objeto . Todos los objetos que pueden tener efectos aplicados implementan esta interfaz; esto incluye orígenes, pistas y composiciones.

Un objeto que implementa esta interfaz puede tener cualquier número de efectos. Para cada objeto, el motor de representación aplica sus efectos en orden de prioridad, empezando por el nivel de prioridad 0.

## <a name="members"></a>Members

La **interfaz IAMTimelineEffectable** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineEffectable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineEffectable** tiene estos métodos.



| Método                                                                     | Descripción                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EffectGetCount**](iamtimelineeffectable-effectgetcount.md)             | Recupera el número de efectos en este objeto.<br/>                    |
| [**EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)           | Inserta un efecto en el objeto en el nivel de prioridad especificado.<br/> |
| [**EffectSwapPriorities**](iamtimelineeffectable-effectswappriorities.md) | Cambia los niveles de prioridad de dos efectos.<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | Recupera el efecto en el nivel de prioridad especificado.<br/>              |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
