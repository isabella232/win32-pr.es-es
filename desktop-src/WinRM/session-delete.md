---
title: Método Session.Delete (WSManDisp.h)
description: Elimina el recurso especificado en el URI del recurso.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Eliminación del método Windows administración remota
- Delete method Windows Remote Management , Session object
- Objeto de sesión Windows administración remota, método Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 769ef3f462fa542e9afc6859b564e1a32ed87578894df4008fb6a19ad8aadad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858675"
---
# <a name="sessiondelete-method"></a>Método Session.Delete

Elimina el recurso especificado en el URI del recurso.

## <a name="syntax"></a>Sintaxis


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resourceUri* \[ En\]
</dt> <dd>

Uri del recurso que se va a eliminar. También puede usar un [**objeto ResourceLocator**](resourcelocator.md) para especificar el recurso.

</dd> <dt>

*flags* \[ in, opcional\]
</dt> <dd>

Reservado para uso futuro. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La sintaxis siguiente se usa para llamar a este método.


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se eliminan los agentes de escucha configurados para el transporte HTTP.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
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

[**Sesión**](session.md)
</dt> </dl>

 

 





