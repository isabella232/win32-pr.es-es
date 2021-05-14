---
description: Obtiene el uso actual del disco del usuario, en bytes.
title: DiDiskQuotaUser.QuotaUsed, propiedad
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
ms.openlocfilehash: a08d7579ad4de51fbc88b7091f2f906ace838883
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841576"
---
# <a name="didiskquotauserquotaused-property"></a>DiDiskQuotaUser.QuotaUsed, propiedad

Obtiene el uso actual del disco del usuario, en bytes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Valor de propiedad

Valor **entero** que se establece en la cantidad de espacio en disco actualmente en uso. Si la compresión de archivos NTFS está habilitada, **QuotaUsed** refleja la cantidad de espacio en disco que los datos requerirían en un estado sin comprimir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**QuotaUsedText**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




