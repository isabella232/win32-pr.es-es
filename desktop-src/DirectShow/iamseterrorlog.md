---
description: La interfaz IAMSetErrorLog establece o recupera un registro de errores en DirectShow Editing Services (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interfaz IAMSetErrorLog (Qedit.h)
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
ms.openlocfilehash: 8a16e56de7f350b30c1b92c0c94ff3e3e06afc31b363c0b3a6e98017ce483aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756405"
---
# <a name="iamseterrorlog-interface"></a>Interfaz IAMSetErrorLog

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMSetErrorLog` interfaz establece o recupera un registro de errores en DirectShow Editing [Services](directshow-editing-services.md) (DES). El objeto timeline implementa esta interfaz. Las aplicaciones pueden usar esta interfaz para registrar errores de representación en tiempo de ejecución. Implemente [**la interfaz IAMErrorLog**](iamerrorlog.md) en la aplicación y, a continuación, llame al método [**IAMSetErrorLog::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) en la escala de tiempo.

Para obtener más información sobre el uso de esta interfaz, vea [Errores de registro.](logging-errors.md)

## <a name="members"></a>Miembros

La **interfaz IAMSetErrorLog** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMSetErrorLog** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMSetErrorLog** tiene estos métodos.



| Método                                               | Descripción                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [**get \_ ErrorLog**](iamseterrorlog-get-errorlog.md) | Recupera el registro de errores actual para este objeto.<br/> |
| [**put \_ ErrorLog**](iamseterrorlog-put-errorlog.md) | Especifica un registro de errores para el objeto .<br/>           |



 

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



 

 
