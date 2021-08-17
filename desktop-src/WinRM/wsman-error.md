---
title: Propiedad WSMan.Error (WSManDisp.h)
description: Obtiene información de error adicional, en una secuencia XML, para la llamada anterior a un método WSMan si Windows un servicio de administración remota no pudo crear un objeto Session, un objeto ConnectionOptions o un objeto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Propiedad de error Windows administración remota
- Propiedad error Windows administración remota , objeto WSMan
- Objeto WSMan Windows administración remota, propiedad Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d72c99150d3c6ac95e91e6a9674ab6364e8ea46fabf3d58d50556e129933cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742200"
---
# <a name="wsmanerror-property"></a>WSMan.Error, propiedad

Obtiene información de error adicional, en una secuencia XML, para la llamada anterior a un método [**WSMan**](wsman.md) si Windows un servicio de administración remota no pudo crear un objeto [**Session,**](session.md) un objeto [**ConnectionOptions**](connectionoptions.md) o un objeto [**ResourceLocator.**](resourcelocator.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>Valor de propiedad

Representación XML de la información de error.

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
</dt> </dl>

 

 





