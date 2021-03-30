---
title: LogFiles. Item (propiedad)
description: Recupera la instancia de LogFileItem especificada de la colección.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Propiedad del elemento SysMon
- Propiedad de elemento SysMon, clase LogFiles
- Clase logfiles SysMon, propiedad Item
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079104"
---
# <a name="logfilesitem-property"></a>LogFiles. Item (propiedad)

Recupera la instancia de [**LogFileItem**](logfileitem.md) especificada de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Valor de propiedad

Instancia de [**LogFileItem**](logfileitem.md) que corresponde al valor de índice especificado.

## <a name="remarks"></a>Observaciones

Esta es la propiedad predeterminada del objeto [**logfiles**](systemmonitor-logfiles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





