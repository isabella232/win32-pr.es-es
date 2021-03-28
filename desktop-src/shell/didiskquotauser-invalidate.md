---
description: Borra la información de usuario almacenada en caché del objeto.
title: DIDiskQuotaUser. Invalidate (método)
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
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540483"
---
# <a name="didiskquotauserinvalidate-method"></a>DIDiskQuotaUser. Invalidate (método)

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

Este método borra la información de usuario almacenada en la memoria caché del objeto. La próxima vez que se realice una solicitud de información relacionada con la cuota, el objeto recuperará la información del volumen NTFS y actualizará la memoria caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




