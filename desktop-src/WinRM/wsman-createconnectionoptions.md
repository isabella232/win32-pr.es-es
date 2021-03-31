---
title: Método WSMan. CreateConnectionOptions (WSManDisp. h)
description: Crea un objeto ConnectionOptions que especifica el nombre de usuario y la contraseña que se usan al crear una sesión.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Método CreateConnectionOptions Administración remota de Windows
- Administración remota de Windows método CreateConnectionOptions, objeto WSMan
- Administración remota de Windows de objeto WSMan, método CreateConnectionOptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905114"
---
# <a name="wsmancreateconnectionoptions-method"></a>WSMan. CreateConnectionOptions (método)

Crea un objeto [**ConnectionOptions**](connectionoptions.md) que especifica el nombre de usuario y la contraseña que se usan al crear una sesión.

## <a name="syntax"></a>Sintaxis


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Un objeto [**ConnectionOptions**](connectionoptions.md) que se usa para especificar un par de nombre de usuario y contraseña que se usa para identificar un usuario para la autenticación.

## <a name="remarks"></a>Observaciones

La siguiente sintaxis se usa para llamar a este método.


```VB
Set options = wsman.CreateConnectionOptions
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
</dt> </dl>

 

 





