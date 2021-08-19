---
title: Estilos de lupa
description: En este tema se describen los estilos usados con el control lupa.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: ef65f736b50210ed52c542375aa340d5bd85ae38265a71858d82e069d830aa62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052583"
---
# <a name="magnifier-styles"></a>Estilos de lupa

En este tema se describen los estilos usados con el control lupa. Para crear un control lupa, use la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) y especifique la clase WC_MAGNIFIER ventana, junto con una combinación de los siguientes estilos de lupa.

| Requisito | Valor |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Recorta el área de la ventana de lupa que rodea el cursor del sistema. Este estilo permite al usuario ver el contenido de la pantalla que está detrás de la ventana de lupa. |
| MS_INVERTCOLORS 0x0004L | Muestra el contenido de la pantalla ampliada con colores invertidos. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Muestra el cursor del sistema ampliado junto con el contenido de la pantalla ampliada. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ampliation.h</dt> </dl> |

## <a name="see-also"></a>Vea también

[Constantes](entry-magapi-constants.md)
