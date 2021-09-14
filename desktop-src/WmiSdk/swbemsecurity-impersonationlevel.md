---
description: La propiedad ImpersonationLevel es un entero que define el nivel de suplantación COM que se asigna a este objeto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Propiedad SWbemSecurity.ImpersonationLevel
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070372"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>Propiedad SWbemSecurity.ImpersonationLevel

La **propiedad ImpersonationLevel** es un entero que define el nivel de suplantación COM que se asigna a este objeto. Esta configuración determina si los procesos propiedad de Windows Management Instrumentation (WMI) pueden detectar o usar sus credenciales de seguridad al realizar llamadas a otros procesos. Para obtener más información sobre los niveles de suplantación, vea [Establecer la seguridad del proceso de aplicación \_ \_ cliente.](setting-client-application-process-security.md)

Si no establece el nivel de suplantación específicamente en un moniker o estableciendo la propiedad **SWBemSecurity.ImpersonationLevel** en un objeto protegible, WMI establece el nivel de suplantación predeterminado en el valor especificado en la clave del Registro de nivel de suplantación [predeterminada.](setting-the-default-process-security-level-using-vbscript.md) Si esta configuración no es suficiente, el proveedor no da servicio a la solicitud y la llamada a la API wmi puede producir un error con un código de error **de wbemErrAccessDenied** (2147749891/0x80041003).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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
| **Anónimo**   | Oculta las credenciales de la persona que llama. WMI no admite realmente este nivel de suplantación; Si un script especifica impersonationLevel=Anonymous, WMI actualizará de forma silenciosa el nivel de suplantación a Identificar. Sin embargo, esto es en cierto modo un ejercicio sin sentido, porque es probable que los scripts que usan el nivel De identificación no se puedan ejecutar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identificar**    | Permite a los objetos consultar las credenciales del autor de la llamada. Es probable que los scripts que usan este nivel de suplantación no se puedan ejecutar; El nivel Identificar normalmente no permite hacer más que comprobar las listas de control de acceso. No podrá ejecutar scripts en equipos remotos mediante Identificar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Permite que los objetos usen las credenciales del autor de la llamada. Se recomienda usar este nivel de suplantación con scripts WMI. Cuando lo haga, el script WMI usará sus credenciales de usuario; como resultado, podrá realizar las tareas que pueda realizar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegado**    | Permite a los objetos permitir que otros objetos usen las credenciales del autor de la llamada. La delegación permite que un script use sus credenciales en un equipo remoto y, a continuación, permite que ese equipo remoto use sus credenciales en otro equipo remoto. Aunque puede usar este nivel de suplantación dentro de los scripts WMI, solo debe hacerlo si es necesario porque podría suponer un riesgo para la seguridad.<br/> No puede usar el nivel de suplantación Delegado a menos que todas las cuentas de usuario y las cuentas de equipo implicadas en la transacción se hayan marcado como De confianza para la delegación en Active Directory. Esto ayuda a minimizar los riesgos de seguridad. Aunque un equipo remoto puede usar sus credenciales, solo puede hacerlo si tanto él como cualquier otro equipo implicado en la transacción son de confianza para la delegación.<br/> |



 

Como se indicó, la suplantación anónima oculta las credenciales e Identificar permite que un objeto remoto consulte las credenciales, pero el objeto remoto no puede suplantar el contexto de seguridad. (En otras palabras, aunque el objeto remoto sabe quién es, no puede "pretender" ser usted). Normalmente, se producirá un error en los scripts WMI que acceden a equipos remotos mediante una de estas dos configuraciones. De hecho, la mayoría de los scripts que se ejecutan en el equipo local con una de estas dos opciones también producirán un error.

Suplantar permite que el servicio WMI remoto use el contexto de seguridad para realizar la operación solicitada. Normalmente, una solicitud WMI remota que usa la configuración Suplantar se realiza correctamente, siempre que las credenciales tengan privilegios suficientes para realizar la operación prevista. En otras palabras, no puede usar WMI para realizar una acción (de forma remota u otra) que no tenga permiso para realizar fuera de WMI.

Si se establece impersonationLevel en Delegate, el servicio WMI remoto puede pasar las credenciales a otros objetos y, por lo general, se considera un riesgo de seguridad.

Puede establecer el nivel de suplantación de un objeto [**SWbemServices**](swbemservices.md), [**SWbemObject,**](swbemobject.md) [**SWbemObjectSet,**](swbemobjectset.md) [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) estableciendo la **propiedad ImpersonationLevel** en el valor deseado. En el ejemplo siguiente se muestra cómo establecer el nivel de suplantación para un **objeto SWbemObject:**


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



También puede especificar niveles de suplantación como parte de un moniker. En el ejemplo siguiente se establece el nivel de autenticación y el nivel de [**\_ suplantación,**](/windows/desktop/CIMWin32Prov/win32-service)y se recupera una instancia del servicio Win32 .


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
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Establecer la seguridad \_ del proceso de la aplicación \_ cliente](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

