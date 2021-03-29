---
title: Mensaje de TB_CHANGEBITMAP (commctrl. h)
description: Cambia el mapa de bits de un botón de una barra de herramientas.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905685"
---
# <a name="tb_changebitmap-message"></a>\_Mensaje CHANGEBITMAP TB

Cambia el mapa de bits de un botón de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón que va a recibir un nuevo mapa de bits.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base cero de una imagen en la lista de imágenes de la barra de herramientas. El sistema muestra la imagen especificada en el botón. Establezca este parámetro en I \_ IMAGECALLBACK y la barra de herramientas enviará la notificación [**TBN \_ GETDISPINFO**](tbn-getdispinfo.md) para recuperar el índice de la imagen cuando sea necesario.

[Versión 5,81](common-control-versions.md). Establezca este parámetro en I \_ IMAGENONE para indicar que el botón no tiene una imagen. El diseño del botón no incluirá ningún espacio para un mapa de bits, solo texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





