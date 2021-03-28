---
description: Obtiene el nombre del contenedor de cuentas del usuario.
title: Propiedad DIDiskQuotaUser. AccountContainerName
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
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808821"
---
# <a name="didiskquotauseraccountcontainername-property"></a>Propiedad DIDiskQuotaUser. AccountContainerName

Obtiene el nombre del contenedor de cuentas del usuario.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Valor de propiedad

Valor de cadena que se establece en el nombre del contenedor de la cuenta del usuario.

## <a name="remarks"></a>Observaciones

En el caso de las cuentas sin información de servicios de directorio, esta propiedad contiene el nombre de dominio. En el caso de las cuentas con información de servicios de directorio, esta propiedad contiene un nombre canónico con el nombre de objeto de terminación quitado.

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

 

 




