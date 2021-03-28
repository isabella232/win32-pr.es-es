---
description: Obtiene un valor booleano que indica si el archivo de cuota para el volumen se está recompilando actualmente.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Propiedad DiskQuotaControl. QuotaFileRebuilding
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
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984411"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>Propiedad DiskQuotaControl. QuotaFileRebuilding

Obtiene un valor booleano que indica si el archivo de cuota para el volumen se está recompilando actualmente.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad se establece en **true** si se vuelve a generar el archivo de cuota o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El archivo de cuota se vuelve a generar automáticamente cuando las cuotas están habilitadas en el sistema o cuando una o más entradas de usuario se marcan para su eliminación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




