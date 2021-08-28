---
title: Objeto WSMan (WSManDisp.h)
description: Proporciona métodos y propiedades que se usan para crear una sesión, representada por un objeto Session.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows WSMan
- Objeto WSMan Windows administración remota , descrito
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac26be22118a320848ea227643f9c4d3857dc01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475971"
---
# <a name="wsman-object"></a>Objeto WSMan

Proporciona métodos y propiedades que se usan para crear una sesión, representada por un [**objeto Session.**](session.md) Cualquier Windows de administración remota requiere la creación de una sesión que se conecte [**a**](session.md) un equipo remoto, al controlador de administración [*base*](windows-remote-management-glossary.md) (BMC) o al equipo local. Las operaciones incluyen obtener, escribir, enumerar datos o invocar métodos.

## <a name="members"></a>Miembros

El **objeto WSMan** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto WSMan** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a> | Crea un <a href="connectionoptions.md"><strong>objeto ConnectionOptions</strong></a> que especifica el nombre de usuario y la contraseña usados al crear una sesión remota.<br /> | 
| <a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a> | Crea un <a href="resourcelocator.md"><strong>objeto ResourceLocator</strong></a> que puede especificar:<br /><ul><li>Ruta de acceso completa a <a href="windows-remote-management-glossary.md"><em>un recurso</em></a> o a un único fragmento de datos.</li><li>Selector <a href="windows-remote-management-glossary.md"><em>para</em></a> una instancia específica de un recurso.</li><li>Opción <a href="windows-remote-management-glossary.md"><em>que</em></a> proporciona datos adicionales al proveedor de recursos.</li></ul> | 
| <a href="wsman-createsession.md"><strong>CreateSession</strong></a> | Crea un <a href="session.md"><strong>objeto Session</strong></a> que, a continuación, se puede usar para las operaciones de red posteriores.<br /> | 
| <a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a> | Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyDeep</strong> para su uso en el <em>parámetro flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a> | Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> para su uso en el parámetro <em>flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a> | Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyShallow</strong> para su uso en el <em>parámetro flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a> | Devuelve el valor de la constante de enumeración <strong>WSManFlagNonXmlText</strong> para su uso en el parámetro <em>flags</em> del <a href="session-enumerate.md"><strong>método Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a> | Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnEPR</strong> para su uso en el <em>parámetro flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a> | Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnObject</strong> para su uso en el <em>parámetro flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a> | Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnObjectAndEPR</strong> para su uso en el <em>parámetro flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a> | Devuelve una cadena con formato que contiene el texto de un número de error.<br /> | 
| <a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagCredUsernamePassword</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagEnableSPNServerPort</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagNoEncryption</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagSkipCACheck</strong> para su uso en el parámetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagSkipCNCheck</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagUseBasic</strong> para su uso en el <em>parámetro flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagUseDigest</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagUseKerberos</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagUseNegotiate</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagUseNoAuthentication</strong> para su uso en el <em>parámetro flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a> | Devuelve el valor de la marca de autenticación <strong>WSManFlagUTF8</strong> para su uso en el <em>parámetro flags</em> de <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 




 

### <a name="properties"></a>Propiedades

El **objeto WSMan** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**Commandline**](wsman-commandline.md)<br/> | Solo lectura<br/> | Obtiene la línea de comandos no procesada para el proceso de hospedaje actual.<br/> |
| [**Error**](wsman-error.md)<br/>             | Solo lectura<br/> | Obtiene información de error.<br/>                                            |



 

## <a name="remarks"></a>Comentarios

El **objeto WSMan** corresponde a las interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) [**e IWSManEx.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) **WSMan** es el único objeto que se puede crear directamente mediante [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo crear una instancia de un **objeto WSMan.**


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Scripting en Windows administración remota](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtener datos del equipo local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtener datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

