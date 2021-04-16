---
description: La interfaz IAMTimelineSplittable divide un objeto Timeline en los servicios de edición de DirectShow (DES). Los orígenes, los efectos, las transiciones y las pistas implementan esta interfaz.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interfaz IAMTimelineSplittable (QEDIT. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689968"
---
# <a name="iamtimelinesplittable-interface"></a>Interfaz IAMTimelineSplittable

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineSplittable` interfaz divide un objeto Timeline en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). Los orígenes, los efectos, las transiciones y las pistas implementan esta interfaz.

## <a name="members"></a>Miembros

La interfaz **IAMTimelineSplittable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSplittable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineSplittable** tiene estos métodos.



| Método                                             | Descripción                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Divide el objeto en el momento especificado.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Divide el objeto en el momento especificado, especificado como un valor de [**REFTIME**](reftime.md) .<br/> |



 

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



 

 
