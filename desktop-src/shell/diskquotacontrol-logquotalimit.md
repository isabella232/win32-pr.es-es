---
description: Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su límite de cuota asignado.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Propiedad DiskQuotaControl.LogQuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f10710c5a16feb946caa78394d5e57e5d7d4884a50d45dc3e37291f40e7d283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455885"
---
# <a name="diskquotacontrollogquotalimit-property"></a>Propiedad DiskQuotaControl.LogQuotaLimit

Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su límite de cuota asignado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad se establece en **TRUE si** se realiza una entrada del registro de eventos del sistema cuando el usuario supera su límite de cuota, o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




