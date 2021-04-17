---
description: La interfaz IAMErrorLog proporciona un método de devolución de llamada para el registro de errores en los servicios de edición de DirectShow (DES). DES no implementa esta interfaz.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interfaz IAMErrorLog (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679396"
---
# <a name="iamerrorlog-interface"></a>Interfaz IAMErrorLog

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMErrorLog` interfaz proporciona un método de devolución de llamada para el registro de errores en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

DES no implementa esta interfaz. Para realizar el registro de errores, implemente esta interfaz en la aplicación y llame a [**IAMSetErrorLog::p \_ ErrorLog UT**](iamseterrorlog-put-errorlog.md) en la escala de tiempo. Si se produce un error al representar el proyecto, DES llamará al método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) implementado por la aplicación.

DES registra los errores solo cuando se representa un proyecto mediante la interfaz [**IRenderEngine**](irenderengine.md) . Por ejemplo, si guarda un proyecto como un gráfico de filtros de DirectShow (formato. GRF) y reproduce el archivo de gráfico, no hay ningún registro de errores. Para obtener más información sobre el uso de esta interfaz, vea [registrar errores](logging-errors.md).

## <a name="members"></a>Miembros

La interfaz **IAMErrorLog** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMErrorLog** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMErrorLog** tiene estos métodos.



| Método                                   | Descripción               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Registra un error.<br/> |



 

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



 

 
