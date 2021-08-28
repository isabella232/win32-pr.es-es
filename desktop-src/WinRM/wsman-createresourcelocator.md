---
title: Método WSMan.CreateResourceLocator (WSManDisp.h)
description: Crea un objeto ResourceLocator que se puede usar en lugar de especificar un URI de recurso en operaciones de objeto de sesión como Session.Get, Session.Put o Session.Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Método CreateResourceLocator Windows administración remota
- Método CreateResourceLocator Windows administración remota , objeto WSMan
- Objeto WSMan Windows administración remota, método CreateResourceLocator
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
ms.openlocfilehash: 2d78276f40ee6e2e1aff10f17bc9f41bb1d1e4aa32cde68a41842c5cee8b95bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742618"
---
# <a name="wsmancreateresourcelocator-method"></a>Método WSMan.CreateResourceLocator

Crea un [**objeto ResourceLocator**](resourcelocator.md) que se puede usar [](session.md) en lugar de especificar un URI de recurso en operaciones de objeto de sesión como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

## <a name="syntax"></a>Sintaxis


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uri* \[ en, opcional\]
</dt> <dd>

Uri de recurso para el recurso. Para obtener más información sobre las cadenas de URI, vea [Uri de recursos.](resource-uris.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**ResourceLocator**](resourcelocator.md) que se puede usar para realizar operaciones winRM locales o remotas.

## <a name="remarks"></a>Comentarios

Si la **propiedad FragmentDialect** no se especifica en el objeto [**ResourceLocator,**](resourcelocator.md) el valor predeterminado es la especificación XPath 1.0. Para más información, consulte [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se crea un objeto [**ResourceLocator**](resourcelocator.md) y se obtiene el valor de la propiedad **Description** del adaptador de red de la instancia de [**\_ Win32 NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con un índice de "1".


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

