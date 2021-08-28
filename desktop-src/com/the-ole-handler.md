---
title: El controlador OLE
description: Un controlador OLE es un archivo DLL que contiene varios componentes de interacción que se usan para vincular e insertar.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecca46971d3ad4fdea7df6a502b2897439e03817849ad776d3e0b13a213a94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129637"
---
# <a name="the-ole-handler"></a>El controlador OLE

Un *controlador OLE* es un archivo DLL que contiene varios componentes de interacción que se usan para vincular e insertar. Para evitar los gastos de comunicación constante entre procesos entre un contenedor y su servidor, el controlador se carga en el espacio de proceso del contenedor para actuar en nombre de un servidor como una especie de proceso suplente. El controlador OLE administra las solicitudes de contenedor que no requieren la atención de la aplicación de servidor, como las solicitudes de dibujo. Cuando un contenedor solicita algo que el controlador de objetos no puede proporcionar, el controlador se comunica con la aplicación de servidor mediante el mecanismo de comunicación fuera de proceso COM.

Los componentes del controlador OLE incluyen partes de comunicación remota para administrar la comunicación entre el controlador y su servidor, una memoria caché para almacenar los datos de un objeto (junto con información sobre cómo se deben dar formato y mostrar los datos) y un objeto de control que coordina las actividades de los demás componentes del archivo DLL. Además, si un objeto es un vínculo, el archivo DLL también incluye un componente de vinculación o un objeto vinculado *,* que realiza un seguimiento del nombre y la ubicación del origen del vínculo.

OLE proporciona un controlador predeterminado que la mayoría de las aplicaciones usan para vincular e insertar. Si el valor predeterminado no coincide con los requisitos del servidor, puede reemplazar completamente el controlador predeterminado o usar partes de la funcionalidad que proporciona cuando corresponda. En el último caso, el controlador de aplicación se implementa como un objeto agregado compuesto por un nuevo objeto de control y el controlador predeterminado. Los controladores de aplicación/predeterminado combinados también se conocen como *controladores en proceso.* El *controlador de comunicación* remota se usa para los objetos a los que no se asigna un CLSID en el Registro del sistema o que no tienen ningún controlador especificado. Todo lo que se requiere de un controlador para estos tipos de objetos es que pasan información a través del límite del proceso. Para crear una nueva instancia del controlador predeterminado, llame [**a OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler). Para algunas circunstancias especiales, llame [**a OleCreateErevhelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).

Cuando se crea una instancia de un controlador para una clase, no se puede usar para otra. Cuando se usa para un documento compuesto, el controlador OLE implementa las estructuras de datos del lado contenedor cuando se accede a los objetos de una clase determinada de forma remota.

OLE definió el controlador predeterminado para los clientes de servidores locales de documentos compuestos. El controlador predeterminado implementó una serie de interfaces que el servidor típico no tenía. Cuando OLE permitía posteriormente servidores en proceso para documentos compuestos, tenían que crear un asistente de inserción que implementara estas interfaces adicionales para que los clientes pudieran trabajar sin problemas con ellos.

Los diseñadores de marcos que definen e implementan un controlador del lado cliente deben tener en cuenta este problema en su diseño y deben proporcionar un asistente en proceso equivalente por las mismas razones. Incluso si los diseñadores no implementan actualmente interfaces en el controlador que los servidores no exponen, es posible que deban definir un asistente ahora para que puedan agregarlas en el futuro. Como alternativa, se pueden implementar las interfaces adicionales en el propio objeto de servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlador de Client-Side ligero](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




