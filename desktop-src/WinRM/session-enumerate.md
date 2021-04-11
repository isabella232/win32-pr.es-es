---
title: Método Session. Enumerate (WSManDisp. h)
description: Enumera una tabla, una colección de datos o un recurso de registro.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumerar Administración remota de Windows de método
- Enumerar Administración remota de Windows de método, objeto de sesión
- Objeto Session Administración remota de Windows, Enumerate (método)
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
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079143"
---
# <a name="sessionenumerate-method"></a>Session. Enumerate (método)

Enumera una tabla, una colección de datos o un recurso de registro. Para crear una consulta, incluya un parámetro de *filtro* y un parámetro de *dialecto* en una enumeración. También puede usar un objeto [**ResourceLocator**](resourcelocator.md) para crear consultas. Para obtener más información, consulte [enumeración o enumeración de todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md).

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

*resourceUri* \[ de\]
</dt> <dd>

Identificador del recurso que se va a recuperar.

Este parámetro puede contener uno de los siguientes elementos:

-   URI del recurso.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Objeto [**ResourceLocator**](resourcelocator.md) .
-   Una referencia de extremo de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar del protocolo WS-Management. Para obtener más información sobre la especificación pública de [protocolo WS-Management](ws-management-protocol.md), consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*filtro* \[ de en, opcional\]
</dt> <dd>

Filtro que define los elementos del recurso devueltos por la enumeración. Cuando se enumera el recurso, solo se devuelven los elementos que coinciden con los criterios de filtro. Al incluir un parámetro de *filtro* y un parámetro de *dialecto* en una enumeración, la enumeración se convierte en una consulta. Para obtener un ejemplo, consulte [consultar instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md).

Si tiene un objeto [**ResourceLocator**](resourcelocator.md) para el parámetro *resourceURI* , este parámetro no debe usarse.

</dd> <dt>

*dialecto* \[ en, opcional\]
</dt> <dd>

Lenguaje utilizado por el filtro. [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), un subconjunto de SQL utilizado por WMI, es el único lenguaje que se admite.

Si tiene un objeto [**ResourceLocator**](resourcelocator.md) para el parámetro *resourceURI* , este parámetro no debe usarse.

</dd> <dt>

*marcas* \[ de en, opcional\]
</dt> <dd>

Parámetro que debe contener una marca en la enumeración **\_ \_ WSManEnumFlags** . Para obtener más información, vea [constantes de enumeración](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto de [**enumerador**](enumerator.md) que contiene los resultados de la enumeración.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre cómo limitar las llamadas de red durante una enumeración, vea la propiedad [**BatchItems**](session-batchitems.md) .

Tenga en cuenta que si las marcas incluyen las [**constantes de enumeración**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , entonces administración remota de Windows servicio devuelve el error del código de error del **modo de \_ \_ polimorfismo WSMAN \_ \_ no compatible**.

Si se especifica un filtro, debe ser un documento válido con respecto al esquema del recurso. El parámetro Dialect es opcional. Sin embargo, si la cadena de filtro comienza con <, pero no es un fragmento XML, incluya el parámetro de *dialecto* o establezca la marca **WSManFlagNonXmlText** en el parámetro *Flags* . Para obtener más información, vea [**constantes de enumeración**](enumeration-constants.md).

El método de C++ correspondiente es [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se enumeran las instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en un equipo remoto especificado por el nombre de dominio completo (ServerName.domain.com). Tenga en cuenta que liberar el objeto de enumeración borra las solicitudes de enumeración pendientes. La subrutina DisplayOutput usa el archivo de transformación XML de la herramienta de línea de comandos de WinRM (WsmTxt. xsl) para generar los datos en un formato tabular.


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

[Consultar instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

