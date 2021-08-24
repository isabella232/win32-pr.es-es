---
title: Atributo ShadowFilePath
description: El atributo ShadowFilePath es la ruta de acceso completa a un archivo de sombra.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Atributo ShadowFilePath Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf1e8f2eb5cb810004ea219aac62973377111902071beb78eca051df19877f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002155"
---
# <a name="shadowfilepath-attribute"></a>Atributo ShadowFilePath

El **atributo ShadowFilePath** es la ruta de acceso completa a un archivo de sombra.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Comentarios

Un *archivo de sombra* se crea como parte de una conversión de formato de archivo. Es la copia de un archivo que usa el Reproductor cuando el usuario sincroniza el contenido del equipo con un dispositivo que requiere que el contenido esté en el formato de archivo original. Este atributo se establece para que el archivo convertido apunte a la ubicación del archivo de sombra.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Acerca del proceso de conversión**](about-the-conversion-process.md)
</dt> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





