---
title: WM/MediaClassPrimaryID
description: El atributo WM/MediaClassPrimaryID contiene el GUID de la clase multimedia principal.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato multimedia de Windows WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d650c15a861cdf55af07fba6d47fb416d61a56d399b855efc461cddd2f628edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027063"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

El **atributo WM/MediaClassPrimaryID** contiene el GUID de la clase multimedia principal.

## <a name="global-constant"></a>Constante global

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>Tipo de datos

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Este atributo debe establecerse en uno de los valores de la tabla siguiente.



| GUID de clase principal                     | Descripción                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Use para archivos de música. No use para audio que no sea música. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Use para archivos de vídeo.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Se usa para archivos de audio que no son música.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Se usa para archivos que no son audio ni vídeo.               |



 

Al especificar un identificador de clase principal, también debe establecer un identificador de clase secundaria para aclarar el tipo de contenido del archivo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




