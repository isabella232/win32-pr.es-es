---
description: El gráfico está abriendo un archivo o ha terminado de abrir un archivo.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 436a48a90640577504871dfe835d6c81c398680ae070065189cb4031493e7fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079125"
---
# <a name="ec_opening_file"></a>ARCHIVO \_ DE APERTURA DE \_ EC

El gráfico está abriendo un archivo o ha terminado de abrir un archivo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**TRUE** si el gráfico está empezando a abrir un archivo, o **FALSE** si el gráfico ya no abre el archivo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Un filtro puede enviar este evento si dedica mucho tiempo a abrir un archivo. (Por ejemplo, el archivo podría encontrarse en una red). La aplicación puede usar este evento para ajustar su interfaz de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




