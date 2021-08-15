---
description: La propiedad AutoReconnect del objeto SWbemRefresher es un valor booleano que indica si el actualizador se vuelve a conectar automáticamente a un proveedor remoto si la conexión está rota.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Propiedad SWbemRefresher.AutoReconnect (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b1ad11c4362276d5714e54ef3196b246a40de1e26bf8f311f41fb5b5834bab0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312817"
---
# <a name="swbemrefresherautoreconnect-property"></a>Propiedad SWbemRefresher.AutoReconnect

La **propiedad AutoReconnect** del objeto [**SWbemRefresher**](swbemrefresher.md) es un valor booleano que indica si el actualizador se vuelve a conectar automáticamente a un proveedor remoto si la conexión está rota.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

La modificación de esta propiedad solo afecta a los objetos del actualizador que están respaldos por un proveedor de alto rendimiento. Si el proveedor no es un proveedor de alto rendimiento, establecer la propiedad **AutoReconnect** en **TRUE** no tiene ningún efecto porque el objeto [**SWbemRefresher**](swbemrefresher.md) nunca se vuelve a conectar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




