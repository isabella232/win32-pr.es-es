---
description: La interfaz IAMTimelineTransable agrega transiciones a un objeto en DirectShow Editing Services (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interfaz IAMTimelineTransable (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072180"
---
# <a name="iamtimelinetransable-interface"></a>IamTimelineTransable (interfaz)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineTransable` interfaz agrega transiciones a un objeto en [DirectShow Editing Services](directshow-editing-services.md) (DES). Esta interfaz se expone mediante cualquier objeto que pueda tener transiciones aplicadas, incluidas pistas, composiciones y grupos. Un objeto que implementa esta interfaz puede tener cualquier número de transiciones, pero las transiciones no deben superponerse en el tiempo.

> [!Note]  
> El audio no admite transiciones. Los objetos de los grupos de audio pueden exponer la interfaz, pero la aplicación no debe `IAMTimelineTransable` agregar transiciones a ellos.

 

## <a name="members"></a>Members

La **interfaz IAMTimelineTransable** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTransable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineTransable** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Recupera la primera transición que aparece en el momento especificado o posterior.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Recupera la primera transición que aparece a la hora especificada o posterior, con el tiempo especificado como valor **REFTIME.**<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Recupera la transición más cercana a la hora especificada.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Recupera la transición más cercana a la hora especificada, dada como un **valor REFTIME.**<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Agrega una transición al objeto .<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Recupera el número de transiciones en este objeto .<br/>                                                                     |



 

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



 

 
