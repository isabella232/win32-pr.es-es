---
title: Tiendas privadas en línea
description: Tiendas privadas en línea
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Reproductor de Windows Media en línea, privado
- tiendas en línea, privadas
- tiendas en línea de tipo 1, privadas
- tiendas en línea de tipo 2, privadas
- tiendas privadas en línea
- registro, tiendas en línea privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359443"
---
# <a name="private-online-stores"></a>Tiendas privadas en línea

Reproductor de Windows Media 10 o posterior admite tiendas en línea privadas; es decir, almacenes que solo son visibles para determinados usuarios. Para que una tienda privada en línea sea visible para el usuario actual, debe haber una entrada que represente la tienda en línea privada bajo la siguiente clave del Registro.

HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ PrivateServices

La entrada del Registro necesaria debe tener el formato siguiente.



| Nombre                                                         | Tipo           | Value                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Cualquier nombre elegido por la persona que crea la entrada del Registro | **REG \_ DWORD** | Número proporcionado por Microsoft que identifica la tienda privada en línea |



 

El control Reproductor de Windows Media 10 ActiveX solo admite almacenes en línea privados si el control se ejecuta en modo remoto. El control Reproductor de Windows Media 11 ActiveX admite almacenes en línea privados independientemente de si el control se ejecuta en modo remoto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




