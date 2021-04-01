---
title: Método WSMan. CreateResourceLocator (WSManDisp. h)
description: Crea un objeto ResourceLocator que se puede usar en lugar de especificar un URI de recurso en operaciones de objeto de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Método CreateResourceLocator Administración remota de Windows
- Administración remota de Windows método CreateResourceLocator, objeto WSMan
- Administración remota de Windows de objeto WSMan, método CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996305"
---
# <a name="wsmancreateresourcelocator-method"></a>WSMan. CreateResourceLocator (método)

Crea un objeto [**ResourceLocator**](resourcelocator.md) que se puede usar en lugar de especificar un URI de recurso en operaciones de objeto de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador URI* \[ en, opcional\]
</dt> <dd>

El URI de recurso para el recurso. Para obtener más información sobre las cadenas URI, consulte [URI de recursos](resource-uris.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un objeto [**ResourceLocator**](resourcelocator.md) que se puede usar para realizar operaciones WinRM locales o remotas.

## <a name="remarks"></a>Observaciones

Si no se especifica la propiedad **FragmentDialect** en el objeto [**ResourceLocator**](resourcelocator.md) , el valor predeterminado es la especificación XPath 1,0. Para más información, consulte [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se crea un objeto [**ResourceLocator**](resourcelocator.md) y se obtiene el valor de la propiedad **Descripción** del adaptador de red de la instancia de [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con un índice de "1".


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
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

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**De sesión**](session.md)
</dt> </dl>

 

