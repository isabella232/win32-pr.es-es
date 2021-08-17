---
title: Método WSMan.CreateConnectionOptions (WSManDisp.h)
description: Crea un objeto ConnectionOptions que especifica el nombre de usuario y la contraseña usados al crear una sesión.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Método CreateConnectionOptions Windows remote management
- Método CreateConnectionOptions Windows administración remota , objeto WSMan
- Objeto WSMan Windows remote management , método CreateConnectionOptions
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
ms.openlocfilehash: 3a4bd1218fcf6ca228cbc7538434b00b7b4e80d4c5b2df54807e031c11c14f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742672"
---
# <a name="wsmancreateconnectionoptions-method"></a>Método WSMan.CreateConnectionOptions

Crea un [**objeto ConnectionOptions**](connectionoptions.md) que especifica el nombre de usuario y la contraseña usados al crear una sesión.

## <a name="syntax"></a>Sintaxis


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Objeto [**ConnectionOptions**](connectionoptions.md) que se usa para especificar un par de nombre de usuario y contraseña que se usa para identificar a un usuario para la autenticación.

## <a name="remarks"></a>Comentarios

La sintaxis siguiente se usa para llamar a este método.


```VB
Set options = wsman.CreateConnectionOptions
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
</dt> </dl>

 

 





