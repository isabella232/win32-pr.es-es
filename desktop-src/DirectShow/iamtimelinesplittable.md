---
description: La interfaz IAMTimelineSplittable divide un objeto de escala de tiempo en DirectShow Editing Services (DES). Los orígenes, efectos, transiciones y pistas implementan esta interfaz.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interfaz IAMTimelineSplittable (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd9f3ca6b1bdea5f80c117b869163d9a2375d5b434765b5962c6216795dd9e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078975"
---
# <a name="iamtimelinesplittable-interface"></a>Interfaz IAMTimelineSplittable

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineSplittable` interfaz divide un objeto de escala de tiempo DirectShow Editing [Services](directshow-editing-services.md) (DES). Los orígenes, efectos, transiciones y pistas implementan esta interfaz.

## <a name="members"></a>Miembros

La **interfaz IAMTimelineSplittable** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineSplittable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineSplittable** tiene estos métodos.



| Método                                             | Descripción                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Divide el objeto en el momento especificado.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Divide el objeto en el momento especificado, especificado como un [**valor REFTIME.**](reftime.md)<br/> |



 

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



 

 
