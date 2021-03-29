---
description: Obtiene el uso actual del disco del usuario como una cadena de texto.
title: Propiedad DIDiskQuotaUser. QuotaUsedText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984263"
---
# <a name="didiskquotauserquotausedtext-property"></a>Propiedad DIDiskQuotaUser. QuotaUsedText

Obtiene el uso actual del disco del usuario como una cadena de texto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a>Valor de propiedad

Valor de cadena que se establece en la cantidad de espacio en disco que se está usando actualmente. Si está habilitada la compresión de archivos NTFS, esta propiedad refleja la cantidad de espacio en disco que los datos necesitarían en un estado sin comprimir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[**QuotaUsed**](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




