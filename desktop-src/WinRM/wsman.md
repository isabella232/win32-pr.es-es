---
title: Objeto WSMan (WSManDisp. h)
description: Proporciona métodos y propiedades que se usan para crear una sesión, representada por un objeto de sesión.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de objeto WSMan
- Administración remota de Windows de objeto WSMan, descrito
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
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421985"
---
# <a name="wsman-object"></a>WSMan (objeto)

Proporciona métodos y propiedades que se usan para crear una sesión, representada por un objeto de [**sesión**](session.md) . Cualquier operación de Administración remota de Windows requiere la creación de una [**sesión**](session.md) que se conecta a un equipo remoto, un [*controlador de administración de base*](windows-remote-management-glossary.md) (BMC) o el equipo local. Las operaciones incluyen la obtención, escritura, enumeración de datos o la invocación de métodos.

## <a name="members"></a>Miembros

El objeto **WSMan** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **WSMan** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></td>
<td style="text-align: left;">Crea un objeto <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> que especifica el nombre de usuario y la contraseña que se usan al crear una sesión remota.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></td>
<td style="text-align: left;">Crea un objeto <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> que puede especificar:<br/>
<ul>
<li>Ruta de acceso completa a un <a href="windows-remote-management-glossary.md"><em>recurso</em></a> o a un solo dato.</li>
<li>Un <a href="windows-remote-management-glossary.md"><em>selector</em></a> para una instancia específica de un recurso.</li>
<li><a href="windows-remote-management-glossary.md"><em>Opción</em></a> que proporciona datos adicionales al proveedor de recursos.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></td>
<td style="text-align: left;">Crea un objeto de <a href="session.md"><strong>sesión</strong></a> que se puede usar para las operaciones de red subsiguientes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyDeep</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyShallow</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la constante de enumeración <strong>WSManFlagNonXmlText</strong> para su uso en el parámetro <em>Flags</em> del método <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnEPR</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnObject</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnObjectAndEPR</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></td>
<td style="text-align: left;">Devuelve una cadena con formato que contiene el texto de un número de error.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagCredUsernamePassword</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagEnableSPNServerPort</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagNoEncryption</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagSkipCACheck</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagSkipCNCheck</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseBasic</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseDigest</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseKerberos</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseNegotiate</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseNoAuthentication</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></td>
<td style="text-align: left;">Devuelve el valor de la marca de autenticación <strong>WSManFlagUTF8</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propiedades

El objeto **WSMan** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**CommandLine**](wsman-commandline.md)<br/> | Solo lectura<br/> | Obtiene la línea de comandos no procesada para el proceso de hospedaje actual.<br/> |
| [**Error**](wsman-error.md)<br/>             | Solo lectura<br/> | Obtiene la información de error.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

El objeto **WSMan** corresponde a las interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) y [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) . **WSMan** es el único objeto que se puede crear directamente mediante [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto **WSMan** .


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de scripting de WinRM](winrm-scripting-api.md)
</dt> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtención de datos del equipo local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

