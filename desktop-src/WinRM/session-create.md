---
title: Método Session. Create (WSManDisp. h)
description: Crea una nueva instancia de un recurso y devuelve la referencia de extremo (EPR) del nuevo objeto.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Crear método Administración remota de Windows
- Create Method Administración remota de Windows, Session (objeto)
- Administración remota de Windows de objeto de sesión, Create (método)
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
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491578"
---
# <a name="sessioncreate-method"></a>Método Session. Create

Crea una nueva instancia de un recurso y devuelve la [*referencia de extremo (EPR)*](windows-remote-management-glossary.md) del nuevo objeto.

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

*resourceUri* \[ de\]
</dt> <dd>

Identificador del recurso que se va a crear.

Este parámetro puede contener uno de los siguientes elementos:

-   URI con uno o más [*selectores*](windows-remote-management-glossary.md). Tenga en cuenta que el [*complemento WMI*](windows-remote-management-glossary.md) no admite la creación de ningún recurso que no sea un agente de escucha de [protocolo WS-Management](ws-management-protocol.md) .
-   Objeto [**ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*Opciones*](windows-remote-management-glossary.md).
-   Referencia de extremo de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar del protocolo WS-Management. Para obtener más información acerca de la especificación pública para el protocolo de WS-Management, consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*resource* 
</dt> <dd>

El XML que contiene el contenido del recurso.

</dd> <dt>

*marcas* \[ de en, opcional\]
</dt> <dd>

Reservado. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El EPR del nuevo recurso.

## <a name="remarks"></a>Observaciones

**Session. Create** solo se usa para crear nuevas instancias de un recurso. Use el método [**Session. put**](session-put.md) para actualizar las instancias existentes de un recurso. Después de obtener el nuevo URI de recurso, puede llamar a [**Session. Get**](session-get.md) para recuperar el nuevo objeto. El nuevo objeto contiene las propiedades que el proveedor de recursos asigna al crear el nuevo objeto. Por ejemplo, si crea una nueva [*escucha*](windows-remote-management-glossary.md) de protocolo de WS-Management y recupera el objeto de agente de escucha mediante **Session. Get**, también obtendrá las **propiedades Port**, **Enabled** y **ListenOn** .

Tenga en cuenta que el [*complemento WMI*](windows-remote-management-glossary.md) no admite la creación de ningún recurso que no sea un agente de escucha del protocolo WS-Management.

La siguiente sintaxis se usa para llamar a este método.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de VBScript llama a **Session. Create** para crear un agente de escucha en el equipo local.


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

[**De sesión**](session.md)
</dt> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

