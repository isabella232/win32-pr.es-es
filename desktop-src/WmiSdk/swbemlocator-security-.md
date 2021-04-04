---
description: La \_ propiedad Security del objeto SWbemLocator se usa para leer o establecer la configuración de seguridad de un objeto SWbemLocator. Esta propiedad es un objeto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Propiedad SWbemLocator.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812421"
---
# <a name="swbemlocatorsecurity_-property"></a>Propiedad SWbemLocator. Security \_

La **propiedad \_ Security** del objeto [**SWbemLocator**](swbemlocator.md) se usa para leer o establecer la configuración de seguridad de un objeto **SWbemLocator** . Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Al establecer la propiedad **\_ Security** de un objeto [**SWbemLocator**](swbemlocator.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento. Para obtener más información, vea [**SWbemSecurity**](swbemsecurity.md).

 

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Las propiedades de un objeto **SWbemLocator. \_ Security** no tienen valores predeterminados. Si intenta obtener el valor de [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) o [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) en un objeto [**SWbemLocator**](swbemlocator.md) antes de establecerlo, se produce un error [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | \_ISWBEMLOCATOR IID<br/>                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Establecer la \_ seguridad del proceso de la aplicación cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**Objeto SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Protección de una conexión WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




