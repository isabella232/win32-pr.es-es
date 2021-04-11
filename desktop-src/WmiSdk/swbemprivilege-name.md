---
description: La propiedad Name de un objeto SWbemPrivilege es una cadena que describe un privilegio de forma única.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Propiedad SWbemPrivilege.Name (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279099"
---
# <a name="swbemprivilegename-property"></a>Propiedad SWbemPrivilege.Name

La propiedad **Name** de un objeto [**SWbemPrivilege**](swbemprivilege.md) es una cadena que describe un privilegio de forma única. Por ejemplo, el privilegio que controla si un usuario puede ejecutar el método Shutdown de un objeto tiene la cadena "SeShutdownPrivilege" en la propiedad **SWbemPrivilege.Name** . Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilege<br/>                                                        |
| IID<br/>                      | \_ISWBEMPRIVILEGE IID<br/>                                                         |



 

 




