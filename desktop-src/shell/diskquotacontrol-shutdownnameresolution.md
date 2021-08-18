---
description: Apaga el subproceso de resolución de nombres de usuario.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Método DiskQuotaControl.ShutdownNameResolution (Dskquota.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da02f79ea8f7b582056e9c3c7c0c3f1db53fa9e08181559c99dd983924861c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459842"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>Método DiskQuotaControl.ShutdownNameResolution

Apaga el subproceso de resolución de nombres de usuario.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El solucionador de nombres de identificador de seguridad (SID) convierte el SID en nombres de usuario en un subproceso en segundo plano. Este subproceso se cierra automáticamente cuando se destruye el objeto de control de cuota asociado. Sin embargo, hay algunos casos en los que el subproceso ya no es necesario, pero el objeto aún no está listo para destruirse. Un ejemplo típico es cuando no se realiza ningún procesamiento adicional, pero los clientes siguen manteniendo referencias al objeto . El **método ShutdownNameResolution** permite finalizar el subproceso de resolución y liberar los recursos asociados sin destruir el objeto de control de cuota.

> [!Note]  
> Al apagar el subproceso de resolución, la resolución de nombres asincrónica se detiene inmediatamente. Si posteriormente se realizan llamadas a métodos como [**AddUser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md), el objeto de cuota podría volver a crear el subproceso de resolución.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




