---
description: Invalida la caché de nombres de usuario del identificador de seguridad.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Método DiskQuotaControl.InvalidateSidNameCache (Dskquota.h)
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
ms.openlocfilehash: 1a171aaaf8f3faa45f967f29bf0f9d742aa0fe0221b46ae4ba4f8527d9cf9715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455895"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>Método DiskQuotaControl.InvalidateSidNameCache

Invalida la caché de nombres de usuario del identificador de seguridad.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Los nombres de usuario y los id. de seguridad asociados se almacenan en una memoria caché. Puede borrar esta memoria caché llamando a **InvalidateSidNameCache.** Si posteriormente crea un nuevo objeto de usuario, la información tendrá que obtenerse del controlador de dominio y la memoria caché tendrá que restablecerse.

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

 

 




