---
description: La propiedad Origin del objeto SWbemProperty recupera el nombre de la clase WMI en la que se introdujo esta propiedad. En el caso de las clases con jerarquías de herencia profundas, a menudo es deseable saber qué propiedades se declararon en qué clases.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Propiedad SWbemProperty.Origin (Wbemdisp.h)
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
ms.openlocfilehash: 3e072267a47ccbcd99ab05544672cf2c1456967cedf97283565a5d8a92aae655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898275"
---
# <a name="swbempropertyorigin-property"></a>Propiedad SWbemProperty.Origin

La **propiedad Origin** del objeto [**SWbemProperty**](swbemproperty.md) recupera el nombre de la clase WMI en la que se introdujo esta propiedad. En el caso de las clases con jerarquías de herencia profundas, a menudo es deseable saber qué propiedades se declararon en qué clases.

Si la propiedad es local (vea [**SWbemQualifier.IsLocal),**](swbemqualifier-islocal.md)este valor es el mismo que la clase propietaria. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




