---
description: La propiedad AuthenticationLevel es un entero que define el nivel de autenticación COM que se asigna a este objeto.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Propiedad SWbemSecurity.AuthenticationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbb765241fabb86a14a5d74f7a839d5d81b017856b6da349b9ec04fd8535a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312719"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>Propiedad SWbemSecurity.AuthenticationLevel

La **propiedad AuthenticationLevel** es un entero que define el nivel de autenticación COM que se asigna a este objeto. Esta configuración determina cómo se protege la información enviada desde WMI. Para obtener más información sobre los niveles de autenticación, vea [Establecer la seguridad del proceso de aplicación \_ \_ cliente.](setting-client-application-process-security.md) En general, no es necesario establecer el nivel de autenticación al realizar llamadas a la API wmi. Si no establece esta propiedad, se usa el nivel de autenticación COM predeterminado para el sistema.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

La configuración authenticationLevel permite solicitar el nivel de autenticación y privacidad de DCOM que se usará a lo largo de una conexión. Configuración de autenticación sin autenticación a autenticación cifrada por paquete.



| Valor        | Descripción                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ninguno         | No usa ninguna autenticación. Se omiten todas las opciones de seguridad.<br/>                                                                                                                                                                                                                                         |
| Valor predeterminado      | Usa una negociación de seguridad estándar para seleccionar un nivel de autenticación. Esta es la configuración recomendada porque el cliente implicado en la transacción se negociará con el nivel de autenticación especificado por el servidor.<br/> DCOM no seleccionará el valor Ninguno durante una sesión de negociación.<br/> |
| Conectar      | Autentica las credenciales del cliente solo cuando el cliente intenta conectarse al servidor. Una vez realizada una conexión, no se realizan comprobaciones de autenticación adicionales.<br/>                                                                                                                          |
| Call         | Autentica las credenciales del cliente solo al principio de cada llamada, cuando el servidor recibe la solicitud. Los encabezados de paquete están firmados, pero los paquetes de datos intercambiados entre el cliente y el servidor no están firmados ni cifrados.<br/>                                                     |
| Pkt          | Autentica que todos los paquetes de datos se reciben del cliente esperado. Similar a Call; Los encabezados de paquetes están firmados pero no cifrados. Los paquetes no están firmados ni cifrados.<br/>                                                                                                               |
| PktIntegrity | Autentica y comprueba que no se ha modificado ninguno de los paquetes de datos transferidos entre el cliente y el servidor. Todos los paquetes de datos están firmados, lo que garantiza que los paquetes no se han modificado durante el tránsito. Ninguno de los paquetes de datos está cifrado.<br/>                                            |
| PktPrivacy   | Autentica todos los niveles de suplantación anteriores y firma y cifra cada paquete de datos. Esto garantiza que toda la comunicación entre el cliente y el servidor sea confidencial.<br/>                                                                                                                             |



 

Puede establecer el nivel de autenticación de los objetos [**SWbemServices**](swbemservices.md), [**SWbemObject,**](swbemobject.md) [**SWbemObjectSet,**](swbemobjectset.md) [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) estableciendo la propiedad **AuthenticationLevel** en el valor deseado.

En el ejemplo siguiente se muestra cómo establecer el nivel de autenticación para un **objeto SwbemObject.**


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



También puede especificar niveles de autenticación como parte de un moniker. En el ejemplo siguiente se establece el nivel de autenticación y el nivel de suplantación, y se recupera una instancia de [**\_ Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Establecer la seguridad \_ del proceso de la aplicación \_ cliente](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> </dl>

 

