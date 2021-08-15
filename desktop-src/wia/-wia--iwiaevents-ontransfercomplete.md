---
description: Evento que tiene lugar cuando una transferencia de datos se completa correctamente.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento Wia.OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9095302a2f3fe75e1939ebb979ec4aad4d87b0462a5b40997e5523e7313d98e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209279"
---
# <a name="wiaontransfercomplete-event"></a>Evento Wia.OnTransferComplete

Evento que tiene lugar cuando una transferencia de datos se completa correctamente.

## <a name="syntax"></a>Sintaxis


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Elemento* 
</dt> <dd>

Objeto [**Item**](-wia-item.md) transferido.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso y nombre de archivo de la imagen transferida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

WIA notifica al script o a la aplicación cuando una transferencia de datos, imagen o sonido se completa correctamente. Implemente **la subrutina objWia** \_ **OnTransferComplete()** para permitir que el script o la aplicación respondan a la finalización de la transferencia de datos.

Por ejemplo, es posible que desee que un script muestre una imagen después de transferirla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




