---
description: Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su umbral de cuota asignado.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Propiedad DiskQuotaControl. LogQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984243"
---
# <a name="diskquotacontrollogquotathreshold-property"></a>Propiedad DiskQuotaControl. LogQuotaThreshold

Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su umbral de cuota asignado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad se establece en **true** si se realiza una entrada del registro de eventos del sistema cuando el usuario supera su umbral de advertencia de cuota o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




