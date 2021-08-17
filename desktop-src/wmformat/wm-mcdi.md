---
title: WM/MCDI
description: El atributo WM/MCDI contiene el identificador de CD de música. Se trata de un volcado binario de la tabla de contenido del CD que se usa para identificar de forma única el CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato multimedia de Windows WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccf4a081141c1902fe93680937a3196e015e6690acf76d69f3a3d8a016c092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963754"
---
# <a name="wmmcdi"></a>WM/MCDI

El **atributo WM/MCDI** contiene el identificador de CD de música. Se trata de un volcado binario de la tabla de contenido del CD que se usa para identificar de forma única el CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMMCDI

## <a name="data-type"></a>Tipo de datos

**BINARIO DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Este atributo es compatible con el marco ID3, MCDI. La especificación ID3 para el marco MCDI requiere que solo exista uno de estos fotogramas por archivo y que exista un marco TRCK válido. El editor de metadatos no realiza ninguna validación para estas reglas. Además, el tamaño de WM/MCDI no se limita a 804 bytes, como es el marco MCDI ID3.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




