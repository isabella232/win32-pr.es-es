---
title: TB_CHANGEBITMAP mensaje (Commctrl.h)
description: Cambia el mapa de bits de un botón de una barra de herramientas.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166893"
---
# <a name="tb_changebitmap-message"></a>Mensaje \_ DE TB CHANGEBITMAP

Cambia el mapa de bits de un botón de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón que va a recibir un nuevo mapa de bits.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base cero de una imagen en la lista de imágenes de la barra de herramientas. El sistema muestra la imagen especificada en el botón. Establezca este parámetro en I IMAGECALLBACK y la barra de herramientas enviará la notificación \_ [**\_ TBN GETDISPINFO**](tbn-getdispinfo.md) para recuperar el índice de imagen cuando sea necesario.

[Versión 5.81.](common-control-versions.md) Establezca este parámetro en I \_ IMAGENONE para indicar que el botón no tiene una imagen. El diseño del botón no incluirá ningún espacio para un mapa de bits, solo texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





