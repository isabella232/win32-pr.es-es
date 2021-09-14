---
description: La interfaz IAMTimelineSplittable divide un objeto de escala de tiempo en DirectShow Editing Services (DES). Los orígenes, los efectos, las transiciones y los seguimientos implementan esta interfaz.
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
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061631"
---
# <a name="iamtimelinesplittable-interface"></a>Interfaz IAMTimelineSplittable

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineSplittable` interfaz divide un objeto de escala de tiempo en DirectShow Editing [Services](directshow-editing-services.md) (DES). Los orígenes, los efectos, las transiciones y los seguimientos implementan esta interfaz.

## <a name="members"></a>Members

La **interfaz IAMTimelineSplittable** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineSplittable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineSplittable** tiene estos métodos.



| Método                                             | Descripción                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Divide el objeto en el momento especificado.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Divide el objeto en el momento especificado, especificado como un [**valor REFTIME.**](reftime.md)<br/> |



 

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



 

 
