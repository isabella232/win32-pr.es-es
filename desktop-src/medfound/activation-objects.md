---
description: Objetos de activación
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Objetos de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8741cbfa8bc3801a23b4976e60c0a3ad028b0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361193"
---
# <a name="activation-objects"></a>Objetos de activación

Un *objeto de activación* es un objeto auxiliar que se usa para crear otro objeto, algo similar a un generador de clases. Los objetos de activación exponen [**la interfaz DESACTIVATE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

Un objeto de activación permite aplazar la creación del objeto de destino, ya que se puede mantener en un puntero [**RECORDSETActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) sin crear el objeto de destino. Los objetos de activación también se pueden serializar y, por tanto, se usan para crear el objeto de destino en otro proceso. Por ejemplo, los objetos de activación se usan para serializar los componentes de canalización del proceso de aplicación al proceso de ruta de acceso multimedia protegida (PMP). Algunas funciones de enumeración también usan los objetos de activación que devuelven una lista de punteros **DE LAACTIVATE.** Antes de que la aplicación cree el objeto de destino, puede obtener información sobre el objeto mediante el examen de atributos en el objeto de activación.

Para crear el objeto de destino a partir de un objeto de activación, llame al [**método IMFActivate::ActivateObject.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) El autor de la llamada [**debe llamar a IMFActivate::ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) cuando haya terminado con el objeto creado. A menudo, la aplicación crea el objeto de activación y la sesión multimedia llama **a ActivateObject**. En ese caso, la sesión multimedia, no la aplicación, debe llamar **a ShutdownObject**. En otras situaciones, la aplicación recibe un puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) de la sesión multimedia y la aplicación llama a **ActivateObject** y **ShutdownObject**. (Por ejemplo, vea [Cómo reproducir archivos multimedia protegidos).](how-to-play-protected-media-files.md)

Los objetos de activación pueden tener atributos y la [**interfaz IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) hereda la [**interfazATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Algunos objetos de activación usan atributos para configurar el objeto creado. Los atributos específicos admitidos por cada objeto se documentan en la referencia de la función de creación de ese objeto de activación. Establezca los atributos mediante el **puntero DE HECHOActivate** que recibe de la función.

Para la reproducción protegida, los objetos de activación se serializan en el proceso PMP. Para admitir la serialización, un objeto de activación debe exponer la **interfaz IPersistStream.** Además, tanto el objeto de activación como el objeto creado deben ser componentes de confianza si el PMP se ejecuta en un proceso protegido. Esto no es un requisito cuando el PMP se carga en un proceso sin protección.

Para usar un objeto de canalización personalizado (como un receptor multimedia) dentro del proceso PMP, debe implementar un objeto de activación para el objeto de canalización:

-   El objeto de activación debe exponer [**LAACTIVATE Y**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) **IPersistStream**.
-   El método **IPersist::GetClassID** del objeto de activación debe devolver el CLSID del objeto de activación.
-   Opcionalmente, puede implementar los **métodos IPersistStream::Save** e **IPersistStream::Load** para serializar los datos que necesite para configurar el objeto de activación.

Cuando la sesión multimedia carga la topología dentro del proceso de PMP, llama a **CoCreateInstance** para crear una nueva instancia del objeto de activación. A continuación, [**llama a RECORDSETActivate::ActivateObject para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) crear el objeto de canalización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation API de plataforma de aplicaciones](media-foundation-platform-apis.md)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



