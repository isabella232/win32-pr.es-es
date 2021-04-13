---
title: Acceder a metadatos y atributos en la aplicación
description: Obtener y establecer metadatos y atributos en la aplicación
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Administrador de dispositivos de Windows Media, metadatos
- Administrador de dispositivos, metadatos
- Guía de programación, metadatos
- aplicaciones de escritorio, metadatos
- crear aplicaciones de Windows Media Administrador de dispositivos, metadatos
- metadata
- Windows Media Administrador de dispositivos, atributos
- Administrador de dispositivos, atributos
- Guía de programación, atributos
- aplicaciones de escritorio, atributos
- crear aplicaciones de Windows Media Administrador de dispositivos, atributos
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "104358544"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>Acceder a metadatos y atributos en la aplicación

En [obtener y establecer metadatos y atributos](getting-and-setting-metadata-and-attributes.md), se ofrece una explicación general de los metadatos y los atributos. En esta sección se tratan las llamadas de método de aplicación específicas para recuperar o establecer valores.

Las aplicaciones pueden recuperar atributos o metadatos sobre un almacenamiento específico mediante una llamada a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata). **GetMetadata** recupera una colección completa de todos los metadatos asociados a un almacenamiento y, a continuación, la aplicación puede enumerar todos los valores o solicitar valores específicos de la colección. **GetSpecifiedMetadata** crea un objeto de metadatos en nombre del autor de la llamada. El autor de la llamada puede solicitar un subconjunto de los datos disponibles rellenando el parámetro *ppwszPropNames* con una matriz de las cadenas de propiedades de Windows Media administrador de dispositivos deseadas y el recuento de la matriz. El objeto de metadatos devuelto se rellenará con las propiedades que se podrían recuperar. Las propiedades que no se pudieron recuperar estarán ausentes. Los metadatos se devuelven en función del mejor esfuerzo.

Un dispositivo puede establecer atributos o metadatos en un almacenamiento mediante una llamada a [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)o [**IWMDMStorage3:: setMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata). Tenga en cuenta que no hay ninguna garantía de que se conserve ningún valor establecido, ya que pueden almacenarse en un almacén de archivos externo no persistente, es posible que no se admitan los valores o que el dispositivo no admita las propiedades como grabable.

También puede obtener o establecer metadatos sobre un dispositivo mediante una llamada a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) o [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty). Hay una tabla independiente de constantes de metadatos de dispositivo que se enumeran al final de las [constantes de metadatos](metadata-constants.md).

En la documentación de referencia de cada método se proporcionan ejemplos de uso de estos métodos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Obtener y establecer metadatos y atributos**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




