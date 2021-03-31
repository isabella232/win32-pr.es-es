---
title: Método Session. Delete (WSManDisp. h)
description: Elimina el recurso especificado en el URI del recurso.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Eliminar método Administración remota de Windows
- Método Delete Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, método Delete
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
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996123"
---
# <a name="sessiondelete-method"></a>Session. Delete (método)

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

*resourceUri* \[ de\]
</dt> <dd>

URI del recurso que se va a eliminar. También puede usar un objeto [**ResourceLocator**](resourcelocator.md) para especificar el recurso.

</dd> <dt>

*marcas* \[ de en, opcional\]
</dt> <dd>

Reservado para uso futuro. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La siguiente sintaxis se usa para llamar a este método.


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
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**De sesión**](session.md)
</dt> </dl>

 

 





