---
title: UI_ALL_COMMANDS (Uiribbon.h)
description: Especifica una constante que identifica la colección de comandos declarada en el archivo de recursos de marcado.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24767f2d3839b94ee83c6a9a527b2e80dcf8c1960e877f65a0e7e96fff4e3ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705964"
---
# <a name="ui_all_commands"></a>COMANDOS \_ DE INTERFAZ DE USUARIO DE \_ TODOS

Especifica una constante que identifica la colección de comandos declarada en el archivo de recursos de marcado.

## <a name="remarks"></a>Comentarios

**Interfaz de usuario \_ ALL \_ COMMANDS** es útil cuando es necesario tener acceso a propiedades similares en todos los comandos. Por ejemplo, **todos \_ \_** los comandos de la interfaz de usuario se pueden pasar a [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) para invalidar y actualizar todos los comandos de la cinta de opciones consultando la aplicación host para obtener nuevos valores de propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma solo para Windows de escritorio de Vista \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma solo para aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |
| Header<br/>                   | <dl> <dt>Uiribbon.h</dt> </dl>                                             |
| Idl<br/>                      | <dl> <dt>Uiribbon.idl</dt> </dl>                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes y enumeraciones](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

