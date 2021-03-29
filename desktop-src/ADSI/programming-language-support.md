---
title: Compatibilidad con el lenguaje de programación
description: Puede escribir aplicaciones cliente ADSI en muchos idiomas.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4946f05806a6e24ff466d08dc141aadf9c995e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903034"
---
# <a name="programming-language-support"></a>Compatibilidad con el lenguaje de programación

Puede escribir aplicaciones cliente ADSI en muchos idiomas. Para la mayoría de las tareas administrativas, ADSI define interfaces y objetos a los que se puede acceder desde los lenguajes compatibles con Automation. Por ejemplo, el sistema de desarrollo de Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) y Java, así como más lenguajes de rendimiento y de eficiencia, como C y C++.

La integración fluida con páginas Active Server y VBScript facilita la escritura de aplicaciones de Internet que tienen acceso a servicios de directorio. Para la integración con aplicaciones de OLE DB, ADSI proporciona un proveedor de OLE DB mediante la compatibilidad con un subconjunto de las interfaces de consulta de OLE DB. El proveedor de OLE DB admite el acceso de solo lectura a Active Directory.

En el caso de las aplicaciones de Internet, el uso de scripting en archivos de páginas Active Server (ASP) puede crear y manipular objetos ADSI en el servidor y mostrar los resultados en una página web. En Microsoft Management Console, los complementos de administración de servicios de directorio pueden usar ADSI para buscar servicios de directorio de interés. En Resumen, Active Directory interfaces de servicio pueden proporcionar acceso a un conjunto amplio y diverso de servicios de directorio, incluidos los que todavía no se han creado.

Para obtener acceso a las estructuras que usan las API tradicionales, la arquitectura ADSI define interfaces de bajo nivel que no admiten la automatización que son accesibles desde lenguajes como C y C++. Estas interfaces son poco más que contenedores COM para los protocolos de red de un servicio de directorio.

La escritura de código en las interfaces publicadas permite a la aplicación tener acceso a los servicios de directorio de todos los proveedores ADSI instalados e integrar los datos resultantes. Con pocos cambios o ningún cambio en el código, la aplicación puede seguir teniendo acceso a servicios de directorio adicionales en la red a medida que se instalan nuevos proveedores de ADSI.

En la siguiente ilustración se muestra cómo se ajusta ADSI en un entorno de aplicación. Tanto si la aplicación se escribe en Visual Basic, en C/C++, en VBScript, en el sistema de desarrollo de Microsoft JScript o como una aplicación web que usa páginas de Active Server, Active Directory interfaces de servicio proporcionan un acceso limpio y fácil de usar a los servicios de directorio subyacentes sin tener que usar las API de red nativas.

![compatibilidad con ADSI para lenguajes de programación](images/ds2layr.png)

Como se muestra en la ilustración anterior, los clientes que no admiten la automatización de tienen acceso a todas las interfaces ADSI, incluidas las interfaces COM puras con la Convención de nomenclatura **IDirectoryXXX** y las interfaces com de automatización con la Convención de nomenclatura **IADsXXX**. Dado que los clientes de principalmente solicitan información de los servicios de directorio, el modelo de consulta flexible de ADSI a través de OLE DB y [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) es efectivo.

 

 




