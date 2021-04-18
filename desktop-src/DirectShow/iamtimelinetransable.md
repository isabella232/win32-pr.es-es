---
description: La interfaz IAMTimelineTransable agrega transiciones a un objeto en los servicios de edición de DirectShow (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interfaz IAMTimelineTransable (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690989"
---
# <a name="iamtimelinetransable-interface"></a>Interfaz IAMTimelineTransable

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineTransable` interfaz agrega transiciones a un objeto en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). Esta interfaz la expone cualquier objeto que puede tener transiciones aplicadas, incluidas las pistas, las composiciones y los grupos. Un objeto que implementa esta interfaz puede tener cualquier número de transiciones, pero las transiciones no deben superponerse en el tiempo.

> [!Note]  
> Audio no admite transiciones. Los objetos dentro de los grupos de audio pueden exponer la `IAMTimelineTransable` interfaz, pero la aplicación no debe agregarles transiciones.

 

## <a name="members"></a>Miembros

La interfaz **IAMTimelineTransable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTransable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineTransable** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Recupera la primera transición que aparece en el momento especificado o posterior.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Recupera la primera transición que aparece en el momento especificado o posterior, con el tiempo dado como valor de **REFTIME** .<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Recupera la transición más cercana a la hora especificada.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Recupera la transición más cercana al tiempo especificado, dado como un valor **REFTIME** .<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Agrega una transición al objeto.<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Recupera el número de transiciones de este objeto.<br/>                                                                     |



 

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



 

 
