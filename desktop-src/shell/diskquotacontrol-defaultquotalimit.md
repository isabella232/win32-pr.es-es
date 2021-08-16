---
description: Establece u obtiene el límite de cuota predeterminado.
title: Propiedad DiskQuotaControl.DefaultQuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7d123bff-5dae-4430-be22-a822e231e43e
ms.openlocfilehash: 87c6bfdf9321b0746cdff96de60f29aa3ec9c93e9c3222d4bc262ae211ece147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860876"
---
# <a name="diskquotacontroldefaultquotalimit-property"></a>Propiedad DiskQuotaControl.DefaultQuotaLimit

Establece u obtiene el límite de cuota predeterminado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaLimit = DiskQuotaControl.DefaultQuotaLimit
DiskQuotaControl.DefaultQuotaLimit = iDefaultQuotaLimit
```



## <a name="property-value"></a>Valor de propiedad

Valor **entero** que especifica o recibe el límite de cuota predeterminado para los nuevos usuarios, en bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




