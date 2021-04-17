---
description: Evento que tiene lugar cuando se completa una transferencia de datos correctamente.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento WIA. OnTransferComplete
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
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276865"
---
# <a name="wiaontransfercomplete-event"></a>Evento WIA. OnTransferComplete

Evento que tiene lugar cuando se completa una transferencia de datos correctamente.

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

Objeto de [**elemento**](-wia-item.md) transferido.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso y nombre de archivo de la imagen transferida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

WIA notifica el script o la aplicación cuando una transferencia de datos, imagen o sonido se completa correctamente. Implemente la subrutina **objWia** \_ **OnTransferComplete ()** para permitir que el script o la aplicación respondan a la finalización de la transferencia de datos.

Por ejemplo, podría querer un script para mostrar una imagen después de transferirla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




