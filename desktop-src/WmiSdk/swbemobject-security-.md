---
description: La propiedad Security del objeto SWbemObject se usa para leer o establecer la configuración de \_ seguridad de un objeto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: SWbemObject.Security_ propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83a155057e445848e727615978c3414e96f63334ffc70c78d5f055a396b53f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313789"
---
# <a name="swbemobjectsecurity_-property"></a>Propiedad SWbemObject.Security \_

La **\_ propiedad Security** del [**objeto SWbemObject**](swbemobject.md) se usa para leer o establecer la configuración de seguridad de **un objeto SWbemObject.** Esta propiedad es un [**objeto SWbemSecurity.**](swbemsecurity.md) La configuración de seguridad de este objeto no indica la autenticación, suplantación o configuración de privilegios realizada en una conexión a Windows Management Instrumentation (WMI) ni la seguridad en vigor para el proxy cuando un objeto se entrega a un receptor en una llamada asincrónica. Para obtener más información, vea [Mantener la seguridad de WMI.](maintaining-wmi-security.md)

> [!Note]  
> Establecer la **propiedad Security \_** de un objeto [**SWbemObject**](swbemobject.md) en **NULL** concede acceso ilimitado a todos los usuarios todo el tiempo. Para obtener más información, [**vea SWbemSecurity**](swbemsecurity.md).

 

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[Crear una aplicación WMI o un script](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Establecer la seguridad \_ del proceso de la aplicación \_ cliente](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilegios**](privilege-constants.md)
</dt> </dl>

 

 




