---
description: La propiedad ImpersonationLevel es un entero que define el nivel de suplantación COM que se asigna a este objeto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: SWbemSecurity. ImpersonationLevel (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913361"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>SWbemSecurity. ImpersonationLevel (propiedad)

La propiedad **ImpersonationLevel** es un entero que define el nivel de suplantación com que se asigna a este objeto. Esta configuración determina si los procesos propiedad de Instrumental de administración de Windows (WMI) pueden detectar o usar sus credenciales de seguridad al realizar llamadas a otros procesos. Para obtener más información sobre los niveles de suplantación, vea [establecer la \_ seguridad del \_ proceso de la aplicación cliente](setting-client-application-process-security.md).

Si no establece el nivel de suplantación específicamente en un moniker o estableciendo la propiedad **SWBemSecurity. ImpersonationLevel** en un objeto protegible, WMI establece el nivel de suplantación predeterminado en el valor especificado en la [clave del registro del nivel de suplantación predeterminado](setting-the-default-process-security-level-using-vbscript.md). Si esta configuración no es suficiente, el proveedor no da servicio a la solicitud y se puede producir un error en la llamada a la API de WMI con un código de error de **wbemErrAccessDenied** (2147749891/0x80041003).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Como nivel de suplantación de DCOM, esta propiedad se puede establecer en uno de los siguientes valores:



| Value           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anónimo**   | Oculta las credenciales de la persona que llama. WMI no admite realmente este nivel de suplantación; Si un script especifica impersonationLevel = Anonymous, WMI actualizará de forma silenciosa el nivel de suplantación para identificar. No obstante, esto se debe a un ejercicio sin sentido, ya que es probable que los scripts que usan el nivel de identificación no funcionen correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identificar**    | Permite que los objetos consulten las credenciales del autor de la llamada. Es probable que se produzcan errores en los scripts que usan este nivel de suplantación. Normalmente, el nivel de identificación permite no tener que comprobar las listas de control de acceso. No podrá ejecutar scripts en equipos remotos mediante la identificación de.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Permite que los objetos usen las credenciales del llamador. Se recomienda usar este nivel de suplantación con scripts de WMI. Al hacerlo, el script de WMI usará sus credenciales de usuario. como resultado, podrá llevar a cabo las tareas que pueda llevar a cabo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegado**    | Permite a los objetos permitir que otros objetos usen las credenciales del llamador. La delegación permite a un script utilizar las credenciales en un equipo remoto y, a continuación, permite a ese equipo remoto usar las credenciales en otro equipo remoto. Aunque puede usar este nivel de suplantación dentro de los scripts de WMI, debe hacerlo solo si es necesario, ya que podría suponer un riesgo para la seguridad.<br/> No se puede usar el nivel de suplantación de delegado a menos que todas las cuentas de usuario y las cuentas de equipo implicadas en la transacción se hayan marcado como de confianza para la delegación en Active Directory. Esto ayuda a minimizar los riesgos de seguridad. Aunque un equipo remoto puede usar sus credenciales, solo puede hacerlo si ambos equipos implicados en la transacción son de confianza para la delegación.<br/> |



 

Como se indicó, la suplantación anónima oculta las credenciales e identifica permite que un objeto remoto consulte sus credenciales, pero el objeto remoto no puede suplantar el contexto de seguridad. (Es decir, aunque el objeto remoto sepa quién es usted, no puede "fingir" que lo sea). Normalmente, se producirá un error en los scripts de WMI que acceden a equipos remotos mediante una de estas dos configuraciones. De hecho, la mayoría de los scripts que se ejecutan en el equipo local con una de estas dos configuraciones también producirán un error.

Impersonate permite al servicio WMI remoto usar el contexto de seguridad para realizar la operación solicitada. Normalmente, una solicitud de WMI remota que usa la configuración de suplantación se realiza correctamente, siempre que las credenciales tengan privilegios suficientes para realizar la operación deseada. En otras palabras, no puede usar WMI para realizar una acción (de forma remota o de otro tipo) que no tenga permiso para realizar fuera de WMI.

Establecer impersonationLevel en Delegate permite al servicio WMI remoto pasar sus credenciales a otros objetos y generalmente se considera un riesgo para la seguridad.

Puede establecer el nivel de suplantación de un objeto [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) estableciendo la propiedad **ImpersonationLevel** en el valor deseado. En el ejemplo siguiente se muestra cómo establecer el nivel de suplantación para un objeto **SWbemObject** :


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



También puede especificar los niveles de suplantación como parte de un moniker. En el ejemplo siguiente se establece el nivel de autenticación y el nivel de suplantación, y se recupera una instancia del [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | \_ISWBEMSECURITY IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Establecer la \_ seguridad del proceso de la aplicación cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

