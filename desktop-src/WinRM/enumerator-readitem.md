---
title: Enumerador. ReadItem (método) (WSManDisp. h)
description: Recupera un elemento del recurso y devuelve una representación XML del elemento.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Método ReadItem Administración remota de Windows
- Método ReadItem Administración remota de Windows, objeto Enumerator
- Objeto enumerador Administración remota de Windows, método ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079144"
---
# <a name="enumeratorreaditem-method"></a>Enumerador. ReadItem (método)

Recupera un elemento del recurso y devuelve una representación XML del elemento.

## <a name="syntax"></a>Sintaxis


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resource* 
</dt> <dd>

URI del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Representación XML del elemento.

## <a name="remarks"></a>Observaciones

Para limitar el número de elementos que se leen, establezca la propiedad [**Session.BatchItems**](session-batchitems.md) .

Tenga en cuenta que la liberación del objeto de enumeración limpia todas las solicitudes de enumeración pendientes.

El método [**Session. Enumerate**](session-enumerate.md) no obtiene una colección de la misma manera que una [consulta WMI](/windows/desktop/WmiSdk/querying-wmi), como `SELECT * from Win32_LogicalDisk` , devuelve una colección en un [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset). Para leer un archivo como una secuencia de texto, cree el objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) scripting y llame al método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para leer cada línea del archivo. De forma similar, se llama al método **Session. Enumerate** para obtener un objeto de [**enumerador**](enumerator.md) y, a continuación, llamar al método **enumerador. ReadItem** . Como en la lectura del archivo de texto, puede comprobar la propiedad [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) para comprobar si ha alcanzado el final de los elementos de datos.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de VBScript llama al método [**Session. Enumerate**](session-enumerate.md) para obtener una lista de los trabajos programados. La subrutina DisplayOutput usa el archivo de transformación XML de la herramienta de línea de comandos WinRM (WsmTxt. xsl) para generar los datos en un formato tabular.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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

[**Enumerador**](enumerator.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

