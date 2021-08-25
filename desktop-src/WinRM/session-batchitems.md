---
title: Session.BatchItems (WSManDisp.h)
description: Establece y obtiene el número de elementos de cada lote de enumeración.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Propiedad BatchItems Windows administración remota
- Propiedad BatchItems Windows administración remota , objeto Session
- Objeto de sesión Windows administración remota, propiedad BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59e395eb27be2b922cf9d53e40f1d8cea0fc13a5dcf7b62b95ac606ec8f3f96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795345"
---
# <a name="sessionbatchitems-property"></a>Session.BatchItems

Establece y obtiene el número de elementos de cada lote de enumeración. Este valor no se puede cambiar durante una enumeración. El proveedor de recursos puede establecer un límite.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Valor de propiedad

Especifica el número máximo de elementos devueltos para cada llamada de red subyacente al servicio. El valor predeterminado es 20.

## <a name="remarks"></a>Comentarios

Se trata de una característica de optimización que controla la frecuencia con la que se realizan llamadas de red entre el cliente y el servidor. Actualmente, solo se usa para enumeraciones. Para obtener más información sobre la enumeración de recursos, vea [**Enumerar**](session-enumerate.md).

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
</dt> <dt>

[**Enumerar**](session-enumerate.md)
</dt> <dt>

[**Enumerator.ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





