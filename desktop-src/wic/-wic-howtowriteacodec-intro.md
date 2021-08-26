---
description: El Windows Imaging Component (WIC) es una plataforma extensible para la creación de imágenes digitales en los sistemas operativos Windows Vista y Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Introducción (Cómo escribir un códec de WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028246c323cfca16760f86f26d3b1d3694a39ff83a27e983320afa96d8fbf771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056515"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a>Introducción (Cómo escribir un códec de WIC-Enabled)

El Windows Imaging Component (WIC) es una plataforma extensible para la creación de imágenes digitales en los sistemas operativos Windows Vista y Windows 7. WIC también está disponible en Windows XP y Windows Server 2003, ya sea como parte de Microsoft .NET Framework 3.0 o como un componente independiente que puede redistribuir. Cualquier aplicación que use WIC puede acceder, mostrar, procesar e imprimir imágenes en cualquier formato de imagen que proporciona un códec habilitado para WIC, mediante un único conjunto de interfaces coherentes que eliminan la necesidad de conocimientos especializados de formatos específicos.

Los Windows Vista Explorer, Windows Vista Galería de fotos, Live Galería de fotos y Windows 7 Visualizador de fotos se basa en WIC. Después de instalar un códec habilitado para WIC en un sistema Windows Vista o Windows 7, el sistema operativo proporciona el mismo nivel de compatibilidad con el formato de imagen asociado que para los formatos de imagen estándar que se incluyen con la plataforma. Dado que escribe el códec para su propio formato de imagen, puede garantizar una calidad coherente siempre que se utilice el formato de imagen y obtener las ventajas de la compatibilidad completa con la plataforma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Funcionamiento del componente Windows creación de imágenes](-wic-howwicworks.md)
</dt> <dt>

Cómo escribir un códec WIC-Enabled datos
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



