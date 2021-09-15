---
description: Windows Imaging Component (WIC) simplifica la administración de colores al proporcionar la interfaz IWICColorContext y la interfaz IWICColorTransform.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Información general sobre la administración de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1552375ee896173ba8d1fdbf4a9ae19c2af6e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466257"
---
# <a name="color-management-overview"></a>Información general sobre la administración de colores

Las imágenes digitales se originan desde y están destinadas a una variedad de dispositivos, cada uno de los cuales tiene su propia gama y rango dinámico. Si un artefacto capturara la misma escena en dos cámaras diferentes, los colores de las imágenes resultantes no aparecerán exactamente iguales, incluso cuando se representan en el mismo dispositivo de salida porque las funcionalidades de gama de colores de los dos dispositivos de origen eran diferentes. Del mismo modo, la misma imagen que se representa en dos dispositivos de destino diferentes aparecerá de forma diferente porque los dispositivos de destino tienen perfiles de color diferentes. Para garantizar la reproducción coherente del color en todos los dispositivos, es necesario crear una asignación del perfil de color del dispositivo de origen al perfil de color del dispositivo de destino. La administración de colores busca generar una coincidencia visual cercana y coherente y es una característica fundamental en la creación de imágenes profesionales.

Poder reproducir de forma coherente el color entre escáneres, monitores, impresoras y aplicaciones suena como un objetivo simple, pero sin un sistema de administración de colores en el sistema operativo, es difícil de lograr. Si cada aplicación es necesaria para generar sus propios perfiles de color, es casi imposible lograr un intercambio de colores coherente a lo largo del proceso de publicación, que incluye análisis, edición y composición, pruebas y distribución.

Windows Imaging Component (WIC) simplifica la administración de colores al proporcionar la [**interfaz IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) y la [**interfaz IWICColorTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) Puede obtener un [**objeto IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) mediante [**IWICFactory::CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer). [**IWICColorContext es**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) una abstracción para el perfil de color del dispositivo. **IWICColorContext** se inicializa con un marco de mapa de bits, el perfil de color del dispositivo de origen y el perfil de color del dispositivo de destino. Realiza la conversión del marco de mapa de bits.

 

 



