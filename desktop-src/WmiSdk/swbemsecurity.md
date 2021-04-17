---
description: El objeto SWbemSecurity obtiene o establece la configuración de seguridad, como los privilegios, las suplantaciones COM y los niveles de autenticación asignados a un objeto.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Objeto SWbemSecurity (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666823"
---
# <a name="swbemsecurity-object"></a>Objeto SWbemSecurity

El objeto **SWbemSecurity** obtiene o establece la configuración de seguridad, como los privilegios, las suplantaciones com y los niveles de autenticación asignados a un objeto. Los objetos [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)y [**SWbemEventSource**](swbemeventsource.md) tienen una propiedad **de \_ seguridad** , que es el objeto **SWbemSecurity** . Al recuperar una instancia o ver el registro de seguridad de WMI, puede que tenga que establecer las propiedades del objeto de **seguridad \_** .

La llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript no puede crear el objeto de seguridad. La configuración de seguridad de este objeto no identifica la configuración de autenticación, suplantación o privilegio en una conexión a WMI, o la seguridad activa para el proxy cuando un objeto se entrega a un receptor en una llamada asincrónica. Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).

## <a name="members"></a>Miembros

El objeto **SWbemSecurity** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **SWbemSecurity** tiene estas propiedades.



| Propiedad                                                                    | Tipo de acceso           | Descripción                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)<br/> | Lectura/escritura<br/> | Valor numérico que define el nivel de autenticación COM que se asigna a este objeto. Esta configuración determina cómo se protege la información enviada desde WMI.<br/>                                                                 |
| [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)<br/>   | Lectura/escritura<br/> | Valor numérico que define el nivel de suplantación COM que se asigna a este objeto. Esta configuración determina si los procesos que pertenecen a WMI pueden detectar o usar sus credenciales de seguridad al realizar llamadas a otros procesos.<br/> |
| [**Privilegios**](swbemsecurity-privileges.md)<br/>                   | Solo lectura<br/>  | Un objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) que define los privilegios para este objeto. Para obtener más información, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).<br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | \_ISWBEMSECURITY IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Establecer la \_ seguridad del proceso de la aplicación cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

