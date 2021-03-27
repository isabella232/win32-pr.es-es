---
description: Invalida la memoria caché de nombres de usuario del identificador de seguridad.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Método DiskQuotaControl. InvalidateSidNameCache (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000983"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>DiskQuotaControl. InvalidateSidNameCache, método

Invalida la memoria caché de nombres de usuario del identificador de seguridad.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los nombres de usuario y los identificadores de seguridad asociados se almacenan en una caché. Puede borrar esta memoria caché mediante una llamada a **InvalidateSidNameCache**. Si posteriormente crea un nuevo objeto de usuario, la información deberá obtenerse del controlador de dominio y se tendrá que restablecer la memoria caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




