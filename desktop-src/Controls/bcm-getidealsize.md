---
title: Mensaje de BCM_GETIDEALSIZE (commctrl. h)
description: Obtiene el tamaño del botón que mejor se adapta a su texto e imagen, si hay una lista de imágenes. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetIdealSize.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- BCM_GETIDEALSIZE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656535"
---
# <a name="bcm_getidealsize-message"></a>\_Mensaje GETIDEALSIZE de BCM

Obtiene el tamaño del botón que mejor se adapta a su texto e imagen, si hay una lista de imágenes. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85)) que recibe el tamaño deseado del botón, incluida la lista de texto e imagen, si está presente. La aplicación que realiza la llamada es responsable de la asignación de esta estructura. Establezca los miembros **CX** y **CY** en cero para que el alto y el ancho idóneos se devuelvan en la estructura de **tamaño** . Para especificar un ancho de botón, establezca el miembro de **CX** en el ancho del botón deseado. El sistema calculará el alto ideal para este ancho y lo devolverá en el miembro **CY** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **true**. En caso contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Si no se desea ningún ancho de botón especial, debe establecer ambos miembros de [**tamaño**](/previous-versions//dd145106(v=vs.85)) en cero para calcular y devolver el alto y ancho ideales. Si el valor del miembro **CX** es mayor que cero, este valor se considera el ancho del botón deseado y se calcula el alto ideal para este ancho y se devuelve en el miembro **CY** .

 

Este mensaje es más aplicable a los pulsadores. Cuando se envía a un botón de pulsación, el mensaje recupera el rectángulo delimitador necesario para mostrar el texto del botón. Además, si el botón de botón tiene una lista de imágenes, también se ajusta el tamaño del rectángulo delimitador para incluir la imagen del botón.

Cuando se envía a un botón de cualquier otro tipo, se recupera el tamaño del rectángulo de ventana del control.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

