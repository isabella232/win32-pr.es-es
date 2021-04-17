---
description: Compatibilidad con proxy para orígenes de red
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Compatibilidad con proxy para orígenes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696678"
---
# <a name="proxy-support-for-network-sources"></a>Compatibilidad con proxy para orígenes de red

Un servidor proxy es un servidor intermedio entre la intranet e Internet, que enruta las solicitudes de la aplicación cliente al servidor multimedia y recupera los archivos del servidor multimedia.

Media Foundation crea implícitamente un objeto de *localizador proxy* cuando una aplicación cliente intenta obtener acceso a una dirección URL de origen. El objeto localizador proxy expone la interfaz [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) . Durante la resolución del código fuente, Media Foundation comprueba el almacén de propiedades pasado al método de resolución de origen.

Si el almacén de propiedades contiene la propiedad [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) establecida en un objeto de generador de localizador proxy implementado por la aplicación, invoca el método [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) para crear un localizador proxy con opciones de configuración personalizadas.

Si no se establece el almacén de propiedades, Media Foundation crea el localizador de proxy con la configuración predeterminada. Estos valores son los siguientes:

-   Si se establece la Directiva de usuario, el localizador proxy utiliza los valores especificados en el registro.

-   Para HTTP, el localizador proxy usa la configuración de proxy del explorador.

-   En el caso de RTSP, el localizador proxy está configurado para omitir los servidores proxy al conectarse al servidor multimedia.

La aplicación puede cambiar esta configuración predeterminada. Los temas siguientes contienen información acerca de los valores de configuración de un localizador proxy:

-   [Opciones de configuración del localizador proxy](proxy-locator-configuration-settings.md)

-   [Cómo configurar el localizador de proxy](how-to-configure-the-proxy-locator.md)

Media Foundation inicializa el localizador de proxy para la dirección URL de origen especificada para la [resolución de origen](source-resolver.md). El localizador proxy detecta un servidor proxy para usarlo en función de los valores de configuración. Cuando el localizador proxy intenta establecer un servidor proxy, registra el resultado de éxito o error en el registro. Este valor se comprueba durante el siguiente proceso de detección del proxy. Si se sabe que un determinado servidor proxy ha causado errores en el pasado, el localizador proxy lo omite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos y propiedades](attributes-and-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



