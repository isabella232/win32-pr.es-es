---
title: Estilos del ampliador
description: En este tema se describen los estilos utilizados con el control ampliador.
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
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422330"
---
# <a name="magnifier-styles"></a>Estilos del ampliador

En este tema se describen los estilos utilizados con el control ampliador. Para crear un control ampliador, utilice la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana WC_MAGNIFIER, junto con una combinación de los siguientes estilos del ampliador.

| Requisito | Value |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Recorta el área de la ventana del ampliador que rodea el cursor del sistema. Este estilo permite al usuario ver el contenido de la pantalla que está detrás de la ventana del ampliador. |
| MS_INVERTCOLORS 0x0004L | Muestra el contenido de la pantalla ampliada con colores invertidos. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Muestra el cursor del sistema ampliado junto con el contenido de la pantalla ampliada. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Aumento de tamaño. h</dt> </dl> |

## <a name="see-also"></a>Vea también

[Constantes](entry-magapi-constants.md)
