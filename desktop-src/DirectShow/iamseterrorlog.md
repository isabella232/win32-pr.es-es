---
description: La interfaz IAMSetErrorLog establece o recupera un registro de errores en los servicios de edición de DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interfaz IAMSetErrorLog (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653521"
---
# <a name="iamseterrorlog-interface"></a>Interfaz IAMSetErrorLog

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMSetErrorLog` interfaz establece o recupera un registro de errores en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). El objeto Timeline implementa esta interfaz. Las aplicaciones pueden utilizar esta interfaz para registrar los errores de representación en tiempo de ejecución. Implemente la interfaz [**IAMErrorLog**](iamerrorlog.md) en la aplicación y, a continuación, llame al método de [**\_ ErrorLog IAMSetErrorLog::p UT**](iamseterrorlog-put-errorlog.md) en la escala de tiempo.

Para obtener más información sobre el uso de esta interfaz, vea [registrar errores](logging-errors.md).

## <a name="members"></a>Miembros

La interfaz **IAMSetErrorLog** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMSetErrorLog** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMSetErrorLog** tiene estos métodos.



| Método                                               | Descripción                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**obtener \_ ErrorLog**](iamseterrorlog-get-errorlog.md) | Recupera el registro de errores actual de este objeto.<br/> |
| [**poner \_ ErrorLog**](iamseterrorlog-put-errorlog.md) | Especifica un registro de errores para el objeto.<br/>           |



 

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



 

 
