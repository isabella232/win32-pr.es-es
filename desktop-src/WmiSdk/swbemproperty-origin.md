---
description: La propiedad Origin del objeto SWbemProperty recupera el nombre de la clase WMI en la que se presentó esta propiedad. En el caso de las clases con jerarquías de herencia profunda, a menudo es conveniente saber qué propiedades se han declarado en cada clase.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Propiedad SWbemProperty. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277123"
---
# <a name="swbempropertyorigin-property"></a>Propiedad SWbemProperty. Origin

La propiedad **Origin** del objeto [**SWbemProperty**](swbemproperty.md) recupera el nombre de la clase WMI en la que se presentó esta propiedad. En el caso de las clases con jerarquías de herencia profunda, a menudo es conveniente saber qué propiedades se han declarado en cada clase.

Si la propiedad es local (vea [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)), este valor es el mismo que el de la clase propietaria. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemProperty.Origin As String
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
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | \_ISWBEMPROPERTY IID<br/>                                                          |



 

 




