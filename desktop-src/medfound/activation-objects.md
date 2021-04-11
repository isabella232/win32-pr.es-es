---
description: Objetos de activación
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Objetos de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8741cbfa8bc3801a23b4976e60c0a3ad028b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154465"
---
# <a name="activation-objects"></a>Objetos de activación

Un *objeto de activación* es un objeto auxiliar que se usa para crear otro objeto, algo similar a un generador de clases. Los objetos de activación exponen la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

Un objeto de activación le permite diferir la creación del objeto de destino, ya que puede incluir en un puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) sin crear el objeto de destino. Los objetos de activación también se pueden serializar y, por tanto, se usan para crear el objeto de destino en otro proceso. Por ejemplo, los objetos de activación se usan para calcular las referencias de los componentes de canalización desde el proceso de aplicación al proceso de la ruta de acceso a medios protegidos (PMP). Los objetos de activación también se usan en ciertas funciones de enumeración que devuelven una lista de punteros **IMFActivate** . Antes de que la aplicación cree el objeto de destino, puede obtener información sobre el objeto examinando los atributos en el objeto de activación.

Para crear el objeto de destino desde un objeto de activación, llame al método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) . El llamador debe llamar a [**IMFActivate:: ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) cuando termine de usar el objeto creado. A menudo, la aplicación crea el objeto de activación y la sesión multimedia llama a **ActivateObject**. En ese caso, la sesión multimedia, no la aplicación, debe llamar a **ShutdownObject**. En otras situaciones, la aplicación recibe un puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) desde la sesión multimedia y la aplicación llama a **ActivateObject** y **ShutdownObject**. (Por ejemplo, vea [Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md)).

Los objetos de activación pueden tener atributos y la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) hereda la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Algunos objetos de activación usan atributos para configurar el objeto creado. Los atributos específicos que admite cada objeto se documentan en la referencia de la función de creación del objeto de activación. Establezca los atributos mediante el puntero **IMFActivate** que recibe de la función.

Para la reproducción protegida, se calculan las referencias de los objetos de activación al proceso de PMP. Para admitir la serialización, un objeto de activación debe exponer la interfaz **IPersistStream** . Además, tanto el objeto de activación como el objeto creado deben ser componentes de confianza si el PMP se está ejecutando en un proceso protegido. Esto no es un requisito cuando el PMP se carga en un proceso sin protección.

Para usar un objeto de canalización personalizado (como un receptor de medios) dentro del proceso de PMP, debe implementar un objeto de activación para el objeto de canalización:

-   El objeto de activación debe exponer [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) y **IPersistStream**.
-   El método **IPersist:: GetClassID** del objeto de activación debe devolver el CLSID del objeto de activación.
-   Opcionalmente, puede implementar los métodos **IPersistStream:: Save** y **IPersistStream:: Load** para calcular las referencias de los datos que necesita para configurar el objeto de activación.

Cuando la sesión multimedia carga la topología dentro del proceso de PMP, llama a **CoCreateInstance** para crear una nueva instancia del objeto de activación. A continuación, llama a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear el objeto de canalización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



