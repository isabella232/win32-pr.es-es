---
title: Método Session.Create (WSManDisp.h)
description: Crea una nueva instancia de un recurso y devuelve la referencia de punto de conexión (EPR) del nuevo objeto.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Creación de métodos Windows administración remota
- Create method Windows Remote Management , Session object
- Objeto de sesión Windows administración remota, método Create
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97adac133adc4c636de395f564927a5f0194b3c52d50685ac034142e6c15aadf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823267"
---
# <a name="sessioncreate-method"></a>Método Session.Create

Crea una nueva instancia de un recurso y devuelve la referencia de punto de conexión [*(EPR)*](windows-remote-management-glossary.md) del nuevo objeto.

## <a name="syntax"></a>Sintaxis


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resourceUri* \[ En\]
</dt> <dd>

Identificador del recurso que se creará.

Este parámetro puede contener uno de los siguientes elementos:

-   URI con uno o varios [*selectores*](windows-remote-management-glossary.md). Tenga en cuenta que el [*complemento WMI*](windows-remote-management-glossary.md) no admite la creación de ningún recurso que no sea protocolo WS-Management agente [de](ws-management-protocol.md) escucha.
-   [**Objeto ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*opciones*](windows-remote-management-glossary.md).
-   Referencia del punto de conexión [*WS-Addressing,*](windows-remote-management-glossary.md) tal y como se describe en el estándar WS-Management protocolo. Para obtener más información sobre la especificación pública para WS-Management, vea Página [de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*resource* 
</dt> <dd>

XML que contiene contenido de recursos.

</dd> <dt>

*flags* \[ in, opcional\]
</dt> <dd>

Reservado. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

EPR del nuevo recurso.

## <a name="remarks"></a>Comentarios

**Session.Create** solo se usa para crear nuevas instancias de un recurso. Use el [**método Session.Put**](session-put.md) para actualizar las instancias existentes de un recurso. Después de obtener el nuevo URI de recurso, puede llamar a [**Session.Get**](session-get.md) para recuperar el nuevo objeto. El nuevo objeto contiene las propiedades que el proveedor de recursos asigna al crear el nuevo objeto. Por ejemplo, si crea un nuevo [](windows-remote-management-glossary.md) agente de escucha de protocolo WS-Management y recupera el objeto de agente de escucha mediante **Session.Get**, también obtiene las propiedades **Port**, **Enabled** y **ListeningOn.**

Tenga en cuenta que el [*complemento WMI*](windows-remote-management-glossary.md) no admite la creación de ningún recurso que no sea WS-Management agente de escucha de protocolo.

La sintaxis siguiente se usa para llamar a este método.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se llama a **Session.Create** para crear un agente de escucha en el equipo local.


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Sesión**](session.md)
</dt> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

