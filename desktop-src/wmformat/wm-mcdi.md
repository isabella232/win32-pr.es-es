---
title: WM/MCDI
description: El atributo WM/MCDI contiene el identificador del CD de música. Se trata de un volcado binario de la tabla de contenido del CD que se usa para identificar de forma única el CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato de Windows Media WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714297"
---
# <a name="wmmcdi"></a>WM/MCDI

El atributo **WM/MCDI** contiene el identificador del CD de música. Se trata de un volcado binario de la tabla de contenido del CD que se usa para identificar de forma única el CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMMCDI

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ binario**

## <a name="remarks"></a>Observaciones

Este atributo es compatible con el marco ID3, MCDI. La especificación ID3 para el marco MCDI requiere que solo exista uno de estos fotogramas por archivo y que exista un fotograma TRCK válido. El editor de metadatos no realiza ninguna validación para estas reglas. Además, el tamaño de WM/MCDI no se limita a 804 bytes, como es el fotograma MCDI ID3.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




