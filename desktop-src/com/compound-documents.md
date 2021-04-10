---
title: Documentos compuestos
description: Los documentos compuestos OLE permiten a los usuarios que trabajan en una sola aplicación manipular los datos escritos en varios formatos y se derivan de varios orígenes.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149677"
---
# <a name="compound-documents"></a>Documentos compuestos

Los documentos compuestos OLE permiten a los usuarios que trabajan en una sola aplicación manipular los datos escritos en varios formatos y se derivan de varios orígenes. Por ejemplo, un usuario podría insertar en un documento de procesamiento de texto un gráfico creado en una segunda aplicación y un objeto de sonido creado en una tercera aplicación. La activación del gráfico hace que la segunda aplicación cargue su interfaz de usuario, o al menos esa parte que contenga las herramientas necesarias para editar el objeto. Al activar el objeto de sonido, la tercera aplicación lo reproduce. En ambos casos, un usuario puede manipular los datos de orígenes externos desde dentro del contexto de un solo documento.

La tecnología de documentos compuestos de OLE se sitúa en una base compuesta por COM, almacenamiento estructurado y transferencia de datos uniforme. Como se resume a continuación, cada una de estas tecnologías principales desempeña un papel fundamental en los documentos compuestos OLE:

<dl> <dt>

<span id="COM"></span><span id="com"></span>COM
</dt> <dd>

Un objeto de documento compuesto es esencialmente un objeto COM que se puede incrustar o vincular a un documento existente. Como objeto COM, un objeto de documento compuesto expone la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , a través de la cual los clientes pueden obtener punteros a sus otras interfaces, incluidas varias, como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)y [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), que proporcionan características especiales exclusivas de los objetos de documento compuestos.

</dd> <dt>

<span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Almacenamiento estructurado
</dt> <dd>

Un objeto de documento compuesto debe implementar las interfaces [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) o, opcionalmente, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) para administrar su propio almacenamiento. Un contenedor que se usa para crear documentos compuestos debe proporcionar la interfaz [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , a través de la cual los objetos almacenan y recuperan datos. Los contenedores casi siempre proporcionan instancias de **IStorage** obtenidas de la implementación de archivos compuestos de OLE. Los contenedores también deben usar las interfaces **IPersistStorage** y/o **IPersistStream** de un objeto.

</dd> <dt>

<span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferencia de datos uniformes
</dt> <dd>

Las aplicaciones que admiten documentos compuestos deben implementar [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , ya que los objetos incrustados y los objetos vinculados comienzan como datos transferidos mediante formatos de Portapapeles OLE especiales, en lugar de formatos de Portapapeles de Microsoft Windows estándar. En otras palabras, el formato de los datos como un objeto incrustado o vinculado es simplemente una opción más proporcionada por el modelo de transferencia de datos uniforme de OLE.

</dd> </dl>

La tecnología de documentos compuestos de OLE beneficia a los desarrolladores de software y a los usuarios. En lugar de sentirse obligado a CRAM cada característica imaginable en una sola aplicación, los desarrolladores de software ahora son gratis, si lo desean, para desarrollar aplicaciones más pequeñas y más centradas que se basan en otras aplicaciones para proporcionar características adicionales. En los casos en los que un desarrollador de software decide proporcionar una aplicación con funcionalidades más allá de sus características principales, el desarrollador puede implementar estos servicios adicionales como archivos dll independientes, que se cargan en la memoria solo cuando se requieren sus servicios. Los usuarios se benefician del software más pequeño, más rápido y más sencillo que pueden combinar y hacer coincidir según sea necesario, manipulando todos los componentes necesarios de dentro de un único documento maestro.

Para obtener más información, vea los temas siguientes:

-   [Contenedores y servidores](containers-and-servers.md)
-   [Vinculación e incrustación](linking-and-embedding.md)
-   [Controladores de objetos](object-handlers.md)
-   [Servidores en proceso](in-process-servers.md)
-   [Objetos y monikers vinculados](linked-objects-and-monikers.md)
-   [Notificaciones](notifications.md)
-   [Interfaces de documentos compuestos](compound-document-interfaces.md)
-   [Estados de objeto](object-states.md)
-   [Implementación de la activación de In-Place](implementing-in-place-activation.md)
-   [Crear objetos vinculados e incrustados a partir de datos existentes](creating-linked-and-embedded-objects-from-existing-data.md)
-   [Ver almacenamiento en caché](view-caching.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> <dt>

[Almacenamiento estructurado](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 