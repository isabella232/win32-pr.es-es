---
title: Tiendas en línea privadas
description: Tiendas en línea privadas
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player tiendas en línea, privado
- tiendas en línea, privado
- tipo 1 tiendas en línea, privado
- tipo 2 tiendas en línea, privado
- tiendas en línea privadas
- registro, almacenes privados en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418889"
---
# <a name="private-online-stores"></a>Tiendas en línea privadas

Windows Media Player 10 o posterior admite tiendas en línea privadas; es decir, los almacenes que solo son visibles para determinados usuarios. Para que una tienda en línea privada sea visible para el usuario actual, debe haber una entrada que represente la tienda en línea privada en la siguiente clave del registro.

HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ PrivateServices

La entrada del registro requerida debe tener el formato siguiente.



| Nombre                                                         | Tipo           | Value                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Cualquier nombre elegido por la persona que crea la entrada del registro | **\_valor DWORD reg** | Un número, proporcionado por Microsoft, que identifica la tienda en línea privada. |



 

El control ActiveX de Windows Media Player 10 solo admite tiendas en línea privadas si el control se está ejecutando en modo remoto. El control ActiveX de Windows Media Player 11 admite almacenes en línea privados, independientemente de si el control se está ejecutando en modo remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




