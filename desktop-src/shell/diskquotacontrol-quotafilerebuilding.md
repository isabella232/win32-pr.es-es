---
description: Obtiene un valor booleano que indica si el archivo de cuota del volumen se está recompilando actualmente.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Propiedad DiskQuotaControl.QuotaFileRebuilding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8e90d5d920392b9b518fed619aeb4f8c7b99d830fad9f6f901c59fe6128ca94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710525"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>Propiedad DiskQuotaControl.QuotaFileRebuilding

Obtiene un valor booleano que indica si el archivo de cuota del volumen se está recompilando actualmente.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad se establece en **TRUE si** se está recompilado el archivo de cuota o **false** en caso contrario.

## <a name="remarks"></a>Comentarios

El archivo de cuota se recompila automáticamente cuando las cuotas están habilitadas en el sistema o cuando una o varias entradas de usuario se marcan para su eliminación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




