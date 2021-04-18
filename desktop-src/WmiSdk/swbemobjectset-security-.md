---
description: La \_ propiedad Security del objeto SWbemObjectSet se usa para obtener o establecer la configuración de seguridad de un objeto SWbemObjectSet. Esta propiedad es un objeto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Propiedad SWbemObjectSet.Security_ (Wbemdisp. h)
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
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706039"
---
# <a name="swbemobjectsetsecurity_-property"></a>Propiedad SWbemObjectSet. Security \_

La **propiedad \_ Security** del objeto [**SWbemObjectSet**](swbemobjectset.md) se usa para obtener o establecer la configuración de seguridad de un objeto **SWbemObjectSet** . Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Al establecer la propiedad [**\_ Security**](swbemobject-security-.md) de un objeto [**SWbemObjectSet**](swbemobjectset.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento. Para obtener más información sobre las implicaciones de acceso ilimitado, vea [**SWbemSecurity**](swbemsecurity.md).

 

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

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
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | \_ISWBEMOBJECTSET IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[Crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Protección de los clientes de scripting](securing-scripting-clients.md)
</dt> </dl>

 

 




