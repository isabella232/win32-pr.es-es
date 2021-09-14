---
title: Compatibilidad con lenguajes de programación
description: Puede escribir aplicaciones cliente ADSI en muchos lenguajes.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4946f05806a6e24ff466d08dc141aadf9c995e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174598"
---
# <a name="programming-language-support"></a>Compatibilidad con lenguajes de programación

Puede escribir aplicaciones cliente ADSI en muchos lenguajes. Para la mayoría de las tareas administrativas, ADSI define interfaces y objetos accesibles desde lenguajes compatibles con Automation. Por ejemplo, el sistema de desarrollo de Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) y Java, así como lenguajes más eficientes y de rendimiento, como C y C++.

La integración fluida Active Server Pages y VBScript facilita la escritura de aplicaciones de Internet que acceden a los servicios de directorio. Para la integración OLE DB aplicaciones, ADSI proporciona un proveedor de OLE DB mediante la compatibilidad con un subconjunto de las interfaces OLE DB consultas. El OLE DB admite el acceso de solo lectura a Active Directory.

Para las aplicaciones de Internet, el uso de scripts en Active Server Page (ASP) puede crear y manipular objetos ADSI en el servidor y mostrar los resultados en una página web. En Microsoft Management Console, los complementos de administración de servicios de directorio pueden usar ADSI para buscar servicios de directorio de interés. En resumen, Active Directory interfaces de servicio pueden proporcionar acceso a un amplio y diverso conjunto de servicios de directorio, incluidos los que aún no se han creado.

Para el acceso a estructuras que usan LAS API tradicionales, la arquitectura adsi define interfaces de bajo nivel que no admiten La automatización es accesible desde lenguajes como C y C++. Estas interfaces son poco más que contenedores COM para protocolos de red para un servicio de directorio.

Escribir código en las interfaces publicadas permite que la aplicación llegue a los servicios de directorio de todos los proveedores adsi instalados e integre los datos resultantes. Con pocos o ningún cambio en el código, la aplicación puede seguir teniendo acceso a servicios de directorio adicionales en la red a medida que se instalan nuevos proveedores adsi.

En la ilustración siguiente se muestra cómo encaja ADSI en un entorno de aplicación. Tanto si la aplicación está escrita en Visual Basic, C/C++, VBScript, el sistema de desarrollo de Microsoft JScript o como una aplicación web que usa Active Server Pages, las interfaces de servicio de Active Directory proporcionan un acceso limpio y fácil de usar a los servicios de directorio subyacentes sin tener que usar las API de red nativas.

![Compatibilidad con adsi para lenguajes de programación](images/ds2layr.png)

Como se muestra en la ilustración anterior, los clientes que no admiten Automation tienen acceso a todas las interfaces ADSI, incluidas las interfaces COM puras con la convención de nomenclatura **IDirectoryXXX** y las interfaces COM de Automation con la convención de nomenclatura **IADsXXX**. Dado que los clientes solicitan principalmente información de los servicios de directorio, el modelo de consulta flexible ADSI a OLE DB [**e IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) es efectivo.

 

 




