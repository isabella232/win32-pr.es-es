---
description: Borra la información de usuario almacenada en caché del objeto.
title: Método DIDiskQuotaUser.Invalidate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 9f8ad77c9697ed5d284cf782f431ec59b38ca415
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843276"
---
# <a name="didiskquotauserinvalidate-method"></a>Método DIDiskQuotaUser.Invalidate

Borra la información de usuario almacenada en caché del objeto.

## <a name="syntax"></a>Sintaxis


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método borra la información del usuario almacenada en la memoria caché del objeto. La próxima vez que se realiza una solicitud de información relacionada con la cuota, el objeto recupera la información del volumen NTFS y actualiza la memoria caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DIDiskQuotaUser (objeto)**](didiskquotauser-object.md)
</dt> </dl>

 

 




