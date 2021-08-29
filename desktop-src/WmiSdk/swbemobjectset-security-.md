---
description: La propiedad Security del objeto SWbemObjectSet se usa para obtener o establecer la configuración de seguridad \_ de un objeto SWbemObjectSet. Esta propiedad es un objeto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: SWbemObjectSet.Security_ propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7e0725fc6aa35043a3a40220b1fb43a3624cfd6ef5b55775adf5f41d26fafe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857217"
---
# <a name="swbemobjectsetsecurity_-property"></a>SWbemObjectSet.Security, propiedad \_

La **\_ propiedad Security** del [**objeto SWbemObjectSet**](swbemobjectset.md) se usa para obtener o establecer la configuración de seguridad de **un objeto SWbemObjectSet.** Esta propiedad es un [**objeto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> Establecer la [**propiedad Security \_**](swbemobject-security-.md) de un objeto [**SWbemObjectSet**](swbemobjectset.md) en **NULL** concede acceso ilimitado a todos los usuarios en todo momento. Para obtener más información sobre las implicaciones del acceso ilimitado, vea [**SWbemSecurity**](swbemsecurity.md).

 

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectSet.Security_ As Object
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
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[Crear una aplicación WMI o un script](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Protección de clientes de scripting](securing-scripting-clients.md)
</dt> </dl>

 

 




