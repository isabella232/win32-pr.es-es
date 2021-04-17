---
description: El componente de creación de imágenes de Windows (WIC) es una plataforma extensible para la creación de imágenes digitales en los sistemas operativos Windows Vista y Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Introducción (cómo escribir un códec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716134"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a>Introducción (cómo escribir un códec WIC-Enabled)

El componente de creación de imágenes de Windows (WIC) es una plataforma extensible para la creación de imágenes digitales en los sistemas operativos Windows Vista y Windows 7. WIC también está disponible en Windows XP y Windows Server 2003, ya sea como parte de Microsoft .NET Framework 3,0 o como un componente independiente que se puede redistribuir. Cualquier aplicación que use WIC puede tener acceso, mostrar, procesar e imprimir imágenes en cualquier formato de imagen que proporcione un códec habilitado para WIC, mediante un único conjunto de interfaces coherentes que eliminan la necesidad de tener conocimientos especializados de formatos específicos.

El explorador de Windows Vista, la Galería fotográfica de Windows Vista, la Galería fotográfica de Windows y el visor de fotografías de Windows 7 se basan en WIC. Después de instalar un códec habilitado para WIC en un sistema Windows Vista o Windows 7, el sistema operativo proporciona el mismo nivel de compatibilidad con el formato de imagen asociado que para los formatos de imagen estándar que se distribuyen con la plataforma. Dado que escribe el códec para su propio formato de imagen, puede garantizar una calidad coherente en cualquier lugar donde se use el formato de la imagen y obtener las ventajas de la compatibilidad total con la plataforma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Cómo funciona el componente de creación de imágenes de Windows](-wic-howwicworks.md)
</dt> <dt>

Cómo escribir un códec de WIC-Enabled
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



