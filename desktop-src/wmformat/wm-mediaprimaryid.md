---
title: WM/MediaClassPrimaryID
description: El atributo WM/MediaClassPrimaryID contiene el GUID de la clase de medio principal.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato de Windows Media WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904191"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

El atributo **WM/MediaClassPrimaryID** contiene el GUID de la clase de medio principal.

## <a name="global-constant"></a>Constante global

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>Tipo de datos

**\_GUID de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo debe establecerse en uno de los valores de la tabla siguiente.



| GUID de clase principal                     | Descripción                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Se usa para archivos de música. No se usa para audio que no sea música. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Se usa para archivos de vídeo.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Se usa para archivos de audio que no son música.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Se usa para los archivos que no son de audio o de vídeo.               |



 

Cuando se especifica un identificador de clase principal, también se debe establecer un identificador de clase secundaria para aclarar el tipo de contenido del archivo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




