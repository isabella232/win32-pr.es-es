---
title: TB_SETWINDOWTHEME mensaje (Commctrl.h)
description: Establece el estilo visual de un control de barra de herramientas.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- TB_SETWINDOWTHEME controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166549"
---
# <a name="tb_setwindowtheme-message"></a>Mensaje \_ SETWINDOWTHEME de TB

Establece el estilo visual de un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena Unicode que contiene el estilo visual de la barra de herramientas que se establece.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

El envío de este mensaje equivale a llamar a [**SetWindowTheme en**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) la barra de herramientas y a su control de información sobre herramientas, si existe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





