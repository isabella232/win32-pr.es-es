---
description: Requisitos para recursos
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Requisitos para recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277995"
---
# <a name="requirements-for-resources"></a>Requisitos para recursos

Dispositivos portátiles de Windows define las siguientes categorías de recursos como valores de **PROPERTYKEY** . Estos valores se usan para describir los recursos individuales de un objeto. El miembro *PID* de la clave de propiedad puede ser diferente para describir los distintos recursos del mismo tipo para todos los tipos, excepto el **\_ \_ valor predeterminado del recurso WPD**, que solo puede describir un recurso. En la página Descripción vinculada de cada tipo de recurso se enumeran los atributos admitidos por ese recurso.



| PROPERTYKEY de recursos                                                | Descripción                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md)              | Especifica el archivo completo detrás del objeto. Este es el único recurso necesario para cualquier objeto con un recurso. |
| [**\_carátula de \_ álbum de recursos de WPD \_**](wpd-resource-album-art.md)         | Especifica una imagen que representa la ilustración del álbum para el objeto.                                           |
| [**\_clip de \_ audio de recursos de WPD \_**](wpd-resource-audio-clip.md)       | Especifica un clip de audio para el objeto.                                                                        |
| [**\_foto de \_ contacto de recursos de WPD \_**](wpd-resource-contact-photo.md) | Especifica una imagen que representa una fotografía de la persona a la que se hace referencia en el objeto de contacto.                |
| [**\_recursos genéricos del recurso WPD \_**](wpd-resource-generic.md)              | Un recurso genérico de tipo de datos undefined. Esto se debe tratar como una matriz de bytes.                             |
| [**\_icono de recurso de WPD \_**](wpd-resource-icon.md)                    | Un icono.                                                                                                       |
| [**\_miniatura de recursos de WPD \_**](wpd-resource-thumbnail.md)          | Imagen en miniatura.                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



