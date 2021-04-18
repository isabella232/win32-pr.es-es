---
title: Atributo ShadowFilePath
description: El atributo ShadowFilePath es la ruta de acceso completa a un archivo de instantáneas.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- ShadowFilePath Media Player de Windows
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653569"
---
# <a name="shadowfilepath-attribute"></a>Atributo ShadowFilePath

El atributo **ShadowFilePath** es la ruta de acceso completa a un archivo de instantáneas.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)

## <a name="remarks"></a>Observaciones

Un *archivo de instantánea* se crea como parte de una conversión de formato de archivo. Es la copia de un archivo que usa el reproductor cuando el usuario sincroniza el contenido del equipo con un dispositivo que requiere que el contenido esté en el formato de archivo original. Este atributo se establece para que el archivo convertido señale a la ubicación del archivo de instantáneas.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Acerca del proceso de conversión**](about-the-conversion-process.md)
</dt> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





