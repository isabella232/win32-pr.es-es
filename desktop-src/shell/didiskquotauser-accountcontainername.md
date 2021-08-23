---
description: Obtiene el nombre del contenedor de cuentas del usuario.
title: Propiedad DIDiskQuotaUser.AccountContainerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: a7a439fe36262e7f73fd7b839fd60af5b1b0a9b05f77769ab1d6a8c5ee9d06fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094240"
---
# <a name="didiskquotauseraccountcontainername-property"></a>Propiedad DIDiskQuotaUser.AccountContainerName

Obtiene el nombre del contenedor de cuentas del usuario.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Valor de propiedad

Valor de cadena que se establece en el nombre del contenedor de la cuenta del usuario.

## <a name="remarks"></a>Comentarios

Para las cuentas sin información de servicios de directorio, esta propiedad contiene el nombre de dominio. Para las cuentas con información de servicios de directorio, esta propiedad contiene un nombre canónico con el nombre del objeto de terminación quitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DIDiskQuotaUser (objeto)**](didiskquotauser-object.md)
</dt> </dl>

 

 




