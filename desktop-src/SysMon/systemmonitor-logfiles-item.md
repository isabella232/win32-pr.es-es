---
title: Propiedad LogFiles.Item
description: Recupera la instancia de LogFileItem especificada de la colección.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Propiedad de elemento SysMon
- Propiedad Item SysMon , clase LogFiles
- Clase LogFiles SysMon , propiedad Item
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
ms.openlocfilehash: b2441575ec45c3d914fef80d5a7c6655b76597c094e319f5f0b01dbb62190e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882286"
---
# <a name="logfilesitem-property"></a>Propiedad LogFiles.Item

Recupera la instancia de [**LogFileItem especificada**](logfileitem.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Valor de propiedad

[**Instancia de LogFileItem**](logfileitem.md) que corresponde al valor de índice especificado.

## <a name="remarks"></a>Comentarios

Esta es la propiedad predeterminada del [**objeto LogFiles.**](systemmonitor-logfiles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





