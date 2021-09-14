---
title: Acceso a metadatos y atributos en la aplicación
description: Obtener y establecer metadatos y atributos en la aplicación
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Archivos Administrador de dispositivos, metadatos
- Administrador de dispositivos,metadata
- guía de programación, metadatos
- aplicaciones de escritorio, metadatos
- crear Windows aplicaciones Administrador de dispositivos multimedia, metadatos
- metadata
- Windows Elementos Administrador de dispositivos, atributos
- Administrador de dispositivos,attributes
- guía de programación, atributos
- aplicaciones de escritorio, atributos
- crear Windows aplicaciones Administrador de dispositivos multimedia, atributos
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967868"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>Acceso a metadatos y atributos en la aplicación

Hay disponible una explicación general de los metadatos y atributos en [Obtención y configuración de metadatos y atributos.](getting-and-setting-metadata-and-attributes.md) En esta sección se tratan llamadas a métodos de aplicación específicos para recuperar o establecer valores.

Las aplicaciones pueden recuperar atributos o metadatos sobre un almacenamiento específico llamando a [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata). **GetMetadata recupera** una colección completa de todos los metadatos asociados a un almacenamiento y, a continuación, la aplicación puede enumerar todos los valores o solicitar valores específicos de la colección. **GetSpecifiedMetadata crea** un objeto de metadatos en nombre del autor de la llamada. El autor de la llamada puede solicitar un subconjunto de los datos disponibles rellenando el parámetro *ppwszPropNames* con una matriz de las cadenas de propiedad Windows Media Administrador de dispositivos deseadas y el recuento de esa matriz. El objeto de metadatos devuelto se rellenará con las propiedades que se podrían recuperar. Las propiedades que no se pudieron recuperar estarán ausentes. Los metadatos se devuelven con el mejor esfuerzo.

Un dispositivo puede establecer atributos o metadatos en un almacenamiento llamando a [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)o [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata). Tenga en cuenta que no hay ninguna garantía de que los valores establecidos se conserven, ya que pueden almacenarse en un almacén de archivos externo no persistente, es posible que los valores no se admitan o que el dispositivo no admita las propiedades como que se pueden escribir.

También puede obtener o establecer metadatos sobre un dispositivo llamando a [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) o [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty). Hay una tabla independiente de constantes de metadatos de dispositivo enumeradas al final de [Constantes de metadatos](metadata-constants.md).

En la documentación de referencia de cada método se proporcionan ejemplos de uso de estos métodos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una Windows de Administrador de dispositivos multimedia**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Obtener y establecer metadatos y atributos**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




