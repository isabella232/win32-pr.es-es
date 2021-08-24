---
description: La interfaz IAMErrorLog proporciona un método de devolución de llamada para el registro de errores en DirectShow Editing Services (DES). DES no implementa esta interfaz.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interfaz IAMErrorLog (Qedit.h)
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
ms.openlocfilehash: f2edd1d315cc7ae35bbc200209667d49d53392ce86a10b40a067182cd0621124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756465"
---
# <a name="iamerrorlog-interface"></a>Interfaz IAMErrorLog

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMErrorLog` interfaz proporciona un método de devolución de llamada para el registro de errores en DirectShow Editing [Services](directshow-editing-services.md) (DES).

DES no implementa esta interfaz. Para realizar el registro de errores, implemente esta interfaz en la aplicación y llame a [**IAMSetErrorLog::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) en la escala de tiempo. Si se produce un error al representar el proyecto, DES llamará al método [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) implementado por la aplicación.

DES registra errores solo cuando se representa un proyecto mediante la [**interfaz IRenderEngine.**](irenderengine.md) Por ejemplo, si guarda un proyecto como un DirectShow de filtro (formato .grf) y reproduce el archivo de grafo, no hay ningún registro de errores. Para obtener más información sobre el uso de esta interfaz, vea [Errores de registro.](logging-errors.md)

## <a name="members"></a>Miembros

La **interfaz IAMErrorLog** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMErrorLog** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMErrorLog** tiene estos métodos.



| Método                                   | Descripción               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Registra un error.<br/> |



 

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



 

 
