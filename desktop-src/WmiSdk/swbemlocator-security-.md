---
description: La propiedad Security del objeto SWbemLocator se usa para leer o establecer la configuración de seguridad de un \_ objeto SWbemLocator. Esta propiedad es un objeto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_ propiedad (Wbemdisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359399"
---
# <a name="swbemlocatorsecurity_-property"></a>Propiedad SWbemLocator.Security \_

La **\_ propiedad Security** del [**objeto SWbemLocator**](swbemlocator.md) se usa para leer o establecer la configuración de seguridad de un **objeto SWbemLocator.** Esta propiedad es un [**objeto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> Establecer la **propiedad Security \_** de un objeto [**SWbemLocator**](swbemlocator.md) en **NULL** concede acceso ilimitado a todos en todo momento. Para obtener más información, [**vea SWbemSecurity**](swbemsecurity.md).

 

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Las propiedades de **un objeto \_ SWbemLocator.Security** no tienen valores predeterminados. Si intenta obtener el valor [**de SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) o [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) en un objeto [**SWbemLocator**](swbemlocator.md) antes de establecerlo, se producirá un error [wbemErrFailed.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Crear una aplicación WMI o un script](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Ejecución de operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Establecer la seguridad \_ del proceso de la aplicación \_ cliente](setting-client-application-process-security.md)
</dt> <dt>

[**Objeto SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Protección de una conexión WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




