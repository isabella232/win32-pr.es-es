---
title: El controlador OLE
description: Un controlador OLE es un archivo DLL que contiene varios componentes interactivos que se usan para vincular e incrustar.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9579f18b44a36a794ff807d9d616dd3a06dd1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075793"
---
# <a name="the-ole-handler"></a>El controlador OLE

Un *controlador OLE* es un archivo DLL que contiene varios componentes interactivos que se usan para vincular e incrustar. Para evitar el gasto de la comunicación constante entre procesos entre un contenedor y su servidor, el controlador se carga en el espacio de proceso del contenedor para que actúe en nombre de un servidor como un tipo de proceso suplente. El controlador OLE administra las solicitudes de contenedor que no requieren la atención de la aplicación de servidor, como las solicitudes de dibujo. Cuando un contenedor solicita algo que el controlador de objetos no puede proporcionar, el controlador se comunica con la aplicación de servidor mediante el mecanismo de comunicación de COM fuera de proceso.

Los componentes de controlador OLE incluyen partes de comunicación remota para administrar la comunicación entre el controlador y su servidor, una memoria caché para almacenar los datos de un objeto (junto con información sobre cómo deben aplicarse formato y mostrar los datos) y un objeto de control que coordina las actividades de los demás componentes del archivo DLL. Además, si un objeto es un vínculo, el archivo DLL también incluye un componente de vinculación, o un *objeto vinculado*, que realiza un seguimiento del nombre y la ubicación del origen del vínculo.

OLE proporciona un controlador predeterminado que la mayoría de las aplicaciones utilizan para vincular e incrustar. Si el valor predeterminado no coincide con los requisitos del servidor, puede reemplazar por completo el controlador predeterminado o usar partes de la funcionalidad que proporciona cuando corresponda. En el último caso, el controlador de la aplicación se implementa como un objeto agregado compuesto por un nuevo objeto de control y por el controlador predeterminado. Los controladores predeterminados o de aplicación combinados también se conocen como *controladores en proceso*. El *controlador de comunicación remota* se utiliza para los objetos que no tienen asignado un CLSID en el registro del sistema o que no tienen un controlador especificado. Todo lo que se necesita de un controlador para estos tipos de objetos es que pasan información a través del límite del proceso. Para crear una nueva instancia del controlador predeterminado, llame a [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler). En algunas circunstancias especiales, llame a [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).

Cuando se crea una instancia de un controlador para una clase, no se puede utilizar para otro. Cuando se usa para un documento compuesto, el controlador OLE implementa las estructuras de datos del contenedor cuando se tiene acceso remoto a los objetos de una clase determinada.

OLE define el controlador predeterminado para los clientes de los servidores locales de documentos compuestos. El controlador predeterminado implementó un número de interfaces que el servidor típico no hizo. Cuando OLE se permite posteriormente en servidores en proceso para documentos compuestos, tenían que crear una aplicación auxiliar de inserción que implementó estas interfaces adicionales para que los clientes pudieran trabajar sin problemas con ellas.

Los diseñadores de marcos que definen e implementan un controlador de cliente deben considerar este problema en su diseño y deben proporcionar una aplicación auxiliar en proceso equivalente por las mismas razones. Incluso si los diseñadores no implementan actualmente interfaces en el controlador que los servidores no exponen, puede que deseen definir una aplicación auxiliar ahora para que puedan agregarlas en el futuro. Como alternativa, puede implementar las interfaces adicionales en el propio objeto de servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




