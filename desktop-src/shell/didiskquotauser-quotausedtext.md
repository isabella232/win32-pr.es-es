---
description: Obtiene el uso actual del disco del usuario como una cadena de texto.
title: Propiedad DIDiskQuotaUser.QuotaUsedText
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
ms.openlocfilehash: 40fca179fd415ca548bdb8b07c16696fde54f165bfde7d373087ec1a763e787c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050678"
---
# <a name="didiskquotauserquotausedtext-property"></a>Propiedad DIDiskQuotaUser.QuotaUsedText

Obtiene el uso actual del disco del usuario como una cadena de texto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a>Valor de propiedad

Valor de cadena que se establece en la cantidad de espacio en disco actualmente en uso. Si la compresión de archivos NTFS está habilitada, esta propiedad refleja la cantidad de espacio en disco que los datos requerirían en un estado sin comprimir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DIDiskQuotaUser (objeto)**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[**QuotaUsed**](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




