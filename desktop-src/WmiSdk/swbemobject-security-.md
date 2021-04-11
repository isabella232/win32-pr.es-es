---
description: La \_ propiedad Security del objeto SWbemObject se usa para leer o establecer la configuración de seguridad para un objeto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Security_ (Wbemdisp. h)
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
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361443"
---
# <a name="swbemobjectsecurity_-property"></a>Propiedad SWbemObject. Security \_

La **propiedad \_ Security** del objeto [**SWbemObject**](swbemobject.md) se usa para leer o establecer la configuración de seguridad para un objeto **SWbemObject** . Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) . La configuración de seguridad de este objeto no indica la configuración de autenticación, suplantación o privilegio realizada en una conexión a Instrumental de administración de Windows (WMI) o la seguridad activa para el proxy cuando un objeto se entrega a un receptor en una llamada asincrónica. Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).

> [!Note]  
> Al establecer la propiedad **\_ Security** de un objeto [**SWbemObject**](swbemobject.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento. Para obtener más información, vea [**SWbemSecurity**](swbemsecurity.md).

 

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Security_ As Object
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
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[Crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Establecer la \_ seguridad del proceso de la aplicación cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilegio**](privilege-constants.md)
</dt> </dl>

 

 




