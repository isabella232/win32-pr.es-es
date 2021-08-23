---
title: Método Session.Enumerate (WSManDisp.h)
description: Enumera una tabla, una recopilación de datos o un recurso de registro.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumerar métodos Windows administración remota
- Enumerar método Windows administración remota , objeto Session
- Objeto de sesión Windows administración remota , Método Enumerate
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc40a45cc28179acd8e5dc9fff17df8b8accddd8dffda3ea299571e11d46564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642635"
---
# <a name="sessionenumerate-method"></a>Método Session.Enumerate

Enumera una tabla, una recopilación de datos o un recurso de registro. Para crear una consulta, incluya un *parámetro de filtro* y un parámetro *dialecto* en una enumeración. También puede usar un [**objeto ResourceLocator**](resourcelocator.md) para crear consultas. Para obtener más información, [vea Enumerar o enumerar todas las instancias de un recurso.](enumerating-or-listing-all-instances-of-a-resource.md)

## <a name="syntax"></a>Sintaxis


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resourceUri* \[ En\]
</dt> <dd>

Identificador del recurso que se va a recuperar.

Este parámetro puede contener uno de los siguientes elementos:

-   URI del recurso.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Objeto [**ResourceLocator.**](resourcelocator.md)
-   Una referencia de punto de conexión de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar WS-Management protocolo. Para obtener más información sobre la especificación pública [para protocolo WS-Management](ws-management-protocol.md), vea Página de índice de [especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*filter* \[ en, opcional\]
</dt> <dd>

Filtro que define qué elementos del recurso devuelve la enumeración . Cuando se enumera el recurso, solo se devuelven los elementos que coinciden con los criterios de filtro. Incluir un *parámetro de* filtro y un *parámetro dialecto* en una enumeración convierte la enumeración en una consulta. Para obtener un ejemplo, vea [Consulta de instancias específicas de un recurso.](querying-for-specific-instances-of-a-resource.md)

Si tiene un objeto [**ResourceLocator**](resourcelocator.md) para el *parámetro resourceURI,* no se debe usar este parámetro.

</dd> <dt>

*dialecto* \[ en, opcional\]
</dt> <dd>

Idioma utilizado por el filtro. [WQL,](/windows/desktop/WmiSdk/wql-sql-for-wmi)un subconjunto de SQL que wmi usa, es el único lenguaje admitido.

Si tiene un objeto [**ResourceLocator**](resourcelocator.md) para el *parámetro resourceURI,* no se debe usar este parámetro.

</dd> <dt>

*flags* \[ en, opcional\]
</dt> <dd>

Parámetro que debe contener una marca en la **\_ \_ enumeración WSManEnumFlags.** Para obtener más información, vea [Constantes de enumeración](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**Enumerator**](enumerator.md) que contiene los resultados de la enumeración .

## <a name="remarks"></a>Comentarios

Para obtener más información sobre cómo limitar las llamadas de red durante una enumeración, vea la [**propiedad BatchItems.**](session-batchitems.md)

Tenga en cuenta que si [](enumeration-constants.md) las marcas incluyen las constantes de enumeración **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow,** Windows servicio de administración remota devuelve el código de **error ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED**.

Si se especifica un filtro, debe ser un documento válido con respecto al esquema del recurso. El parámetro dialect es opcional. Sin embargo, si la cadena de filtro comienza por <, pero no es un fragmento XML, incluya el parámetro *dialecto* o establezca la marca **WSManFlagNonXmlText** en el *parámetro flags.* Para obtener más información, vea [**Constantes de enumeración**](enumeration-constants.md).

El método de C++ correspondiente [**es IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se enumeran las instancias de [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en un equipo remoto especificado por el nombre de dominio completo (servername.domain.com). Tenga en cuenta que al liberar el objeto de enumeración se borran las solicitudes de enumeración pendientes. La subrutina DisplayOutput usa el archivo de transformación XML de la herramienta de línea de comandos Winrm (WsmTxt.xsl) para generar los datos en un formato tabular.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sesión**](session.md)
</dt> <dt>

[Consulta de instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

