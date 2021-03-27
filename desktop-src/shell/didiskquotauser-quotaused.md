---
description: Obtiene el uso actual del disco del usuario, en bytes.
title: Propiedad DIDiskQuotaUser. QuotaUsed
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153911"
---
# <a name="didiskquotauserquotaused-property"></a>Propiedad DIDiskQuotaUser. QuotaUsed

Obtiene el uso actual del disco del usuario, en bytes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Valor de propiedad

Valor **entero** que se establece en la cantidad de espacio en disco que se está usando actualmente. Si está habilitada la compresión de archivos NTFS, **QuotaUsed** refleja la cantidad de espacio en disco que los datos necesitarían en un estado sin comprimir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**QuotaUsedText**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




