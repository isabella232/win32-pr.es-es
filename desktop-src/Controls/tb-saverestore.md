---
title: TB_SAVERESTORE mensaje (Commctrl.h)
description: Envíe este mensaje para iniciar la guardado o restauración de un estado de la barra de herramientas.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166666"
---
# <a name="tb_saverestore-message"></a>Mensaje \_ SAVERESTORE de TB

Envíe este mensaje para iniciar la guardado o restauración de un estado de la barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Guardar o restaurar marca. Si este parámetro es **TRUE**, se guarda la información. Si es **FALSE**, se restaura la información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) que especifica la clave del Registro, la subclave y el nombre de valor para la información de estado de la barra de herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para la versión 4.72 y anteriores, para usar este mensaje para guardar o restaurar una barra de herramientas, la ventana primaria del control de barra de herramientas debe implementar un controlador para el código de [notificación \_ GETBUTTONINFO de TBN.](tbn-getbuttoninfo.md) La barra de herramientas emite esta notificación para recuperar información sobre cada botón a medida que se restaura.

La versión 5.80 incluye una nueva opción de guardar o restaurar. Al principio del proceso y, a medida que se guarde o restaure cada botón, la aplicación recibirá una notificación [ \_ TBN SAVE](tbn-save.md) o [TBN \_ RESTORE.](tbn-restore.md) Para usar esta opción, debe implementar controladores de notificación para proporcionar al Shell la información de mapa de bits y estado que necesita para guardar o restaurar correctamente el estado de la barra de herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ SAVERESTOREW** (Unicode) y **TB \_ SAVERESTOREA** (ANSI)<br/>             |



 

 





