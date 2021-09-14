---
description: Compatibilidad con proxy para orígenes de red
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Compatibilidad con proxy para orígenes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263175"
---
# <a name="proxy-support-for-network-sources"></a>Compatibilidad con proxy para orígenes de red

Un servidor proxy es un servidor intermedio entre la intranet e Internet, que enruta las solicitudes de la aplicación cliente al servidor multimedia y recupera archivos del servidor multimedia.

Media Foundation crea implícitamente un objeto *de localizador de proxy* cuando una aplicación cliente intenta acceder a una dirección URL de origen. El objeto de localizador de proxy expone la [**interfaz IMFNetProxyLocator.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) Durante la resolución de origen, Media Foundation comprueba el almacén de propiedades pasado al método de resolución de origen.

Si el almacén de propiedades contiene la propiedad [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) establecida en un objeto de generador de localizadores de proxy implementado por la aplicación, invoca el método [**MFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) para crear un localizador de proxy con valores de configuración personalizados.

Si no se establece el almacén de propiedades, Media Foundation el localizador de proxy con la configuración predeterminada. Esta configuración es la siguiente:

-   Si se establece la directiva de usuario, el localizador de proxy usa la configuración especificada en el Registro.

-   Para HTTP, el localizador de proxy usa la configuración del proxy del explorador.

-   Para RTSP, el localizador de proxy está configurado para omitir los servidores proxy al conectarse al servidor multimedia.

La aplicación puede cambiar esta configuración predeterminada. Los temas siguientes contienen información sobre los valores de configuración de un localizador de proxy:

-   [Configuración del localizador de proxy Configuración](proxy-locator-configuration-settings.md)

-   [Cómo configurar el localizador de proxy](how-to-configure-the-proxy-locator.md)

Media Foundation inicializa el localizador de proxy para la dirección URL de origen especificada en el [solucionador de origen.](source-resolver.md) El localizador de proxy detecta un servidor proxy que se usará en función de los valores de configuración. Cuando el localizador de proxy intenta establecer un servidor proxy, registra el resultado correcto o de error en el registro. Este valor se comprueba durante el siguiente proceso de detección de proxy. Si se sabe que un servidor proxy determinado ha causado errores en el pasado, el localizador de proxy lo omite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos y propiedades](attributes-and-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



