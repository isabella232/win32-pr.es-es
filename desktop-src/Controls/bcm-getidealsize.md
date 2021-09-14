---
title: BCM_GETIDEALSIZE mensaje (Commctrl.h)
description: Obtiene el tamaño del botón que mejor se adapta a su texto e imagen, si hay una lista de imágenes. Puede enviar este mensaje explícitamente o usar la \_ macro Button GetIdealSize.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- BCM_GETIDEALSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170150"
---
# <a name="bcm_getidealsize-message"></a>Mensaje \_ GETIDEALSIZE de BCM

Obtiene el tamaño del botón que mejor se adapta a su texto e imagen, si hay una lista de imágenes. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetIdealSize.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SIZE**](/previous-versions//dd145106(v=vs.85)) que recibe el tamaño deseado del botón, incluido el texto y la lista de imágenes, si está presente. La aplicación que realiza la llamada es responsable de asignar esta estructura. Establezca los **miembros cx** y **cy** en cero para que el alto y el ancho ideales se devuelvan en la **estructura SIZE.** Para especificar un ancho de botón, establezca el **miembro cx** en el ancho de botón deseado. El sistema calculará el alto ideal para este ancho y lo devolverá en el **miembro cy.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **TRUE.** De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> Si no se desea ningún ancho de botón especial, debe establecer ambos miembros de [**SIZE**](/previous-versions//dd145106(v=vs.85)) en cero para calcular y devolver el alto y ancho ideales. Si el valor del miembro **cx** es mayor que cero, este valor se considera el ancho de botón deseado y el alto ideal para este ancho se calcula y se devuelve en el **miembro cy.**

 

Este mensaje es más aplicable a pushButtons. Cuando se envía a un elemento PushButton, el mensaje recupera el rectángulo delimitador necesario para mostrar el texto del botón. Además, si pushButton tiene una lista de imágenes, el rectángulo delimitador también se dimensiona para incluir la imagen del botón.

Cuando se envía a un botón de cualquier otro tipo, se recupera el tamaño del rectángulo de ventana del control.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

