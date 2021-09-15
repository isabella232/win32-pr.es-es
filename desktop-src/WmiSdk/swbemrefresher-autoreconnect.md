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
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567213"
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

## <a name="remarks"></a>Observaciones

La modificación de esta propiedad solo afecta a los objetos del actualizador que están respaldos por un proveedor de alto rendimiento. Si el proveedor no es un proveedor de alto rendimiento, establecer la propiedad **AutoReconnect** en **TRUE** no tiene ningún efecto porque el objeto [**SWbemRefresher**](swbemrefresher.md) nunca se vuelve a conectar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




