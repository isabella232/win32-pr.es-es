---
title: Definición de interfaces COM
description: Microsoft define muchas interfaces COM. En la mayoría de los casos, puede reutilizar estas interfaces genéricas. Sin embargo, algunas aplicaciones tienen requisitos específicos que hacen que sea deseable o necesario definir sus propias interfaces de objeto.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516c02a2c337b2c76229094b0e42d75b44f65d16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473254"
---
# <a name="defining-com-interfaces"></a>Definición de interfaces COM

Microsoft define muchas interfaces COM. En la mayoría de los casos, puede reutilizar estas interfaces genéricas. Sin embargo, algunas aplicaciones tienen requisitos específicos que hacen que sea deseable o necesario definir sus propias interfaces de objeto.

Todas las interfaces COM deben derivar, directa o indirectamente, de [**la interfaz IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Dentro de esa restricción, la interfaz personalizada puede admitir casi cualquier método o parámetro, incluidos los métodos asincrónicos. También puede generar una biblioteca de tipos para las interfaces personalizadas para que los clientes puedan acceder a información sobre los métodos del objeto en tiempo de ejecución. Después de definir una interfaz, describirla en Lenguaje de definición de interfaz de Microsoft (MIDL), compilarla y registrarla, se usa como cualquier interfaz genérica. Con COM distribuido, los métodos de interfaz están disponibles tanto para los procesos remotos como para otros procesos en el mismo equipo.

Por último, la compilación de interfaces COM requiere un entorno de desarrollo que incluya un compilador de C/C++ y Midl.exe compilador.

Los pasos para crear una interfaz COM son los siguientes:

-   Decida cómo desea proporcionar compatibilidad con la serialización para la interfaz. ya sea con serialización controlada por biblioteca de tipos o con un archivo DLL de proxy o de código auxiliar. Incluso las interfaces en proceso se deben serializar si se van a usar a través de los límites del apartamento. Es una buena idea crear compatibilidad con la serialización en todas las interfaces COM, incluso si no cree que la necesitará. Vea [Serialización de interfaces](interface-marshaling.md) para obtener más información.
-   Describa la interfaz o las interfaces de un archivo de definición de interfaz (IDL). Además, puede especificar determinados aspectos locales de la interfaz en un archivo de configuración de la aplicación (ACF). Si usa la serialización controlada por biblioteca de tipos, agregue una instrucción de biblioteca que haga referencia [**a**](/windows/desktop/Midl/library) las interfaces para las que desea generar información de tipos.
-   Use el compilador MIDL para generar un archivo de biblioteca de tipos y un archivo de encabezado, o archivos proxy/stub en lenguaje C, archivo de identificador de interfaz, archivo de datos DLL y archivo de encabezado. Vea [Compilación MIDL](midl-compilation.md) para obtener más información.
-   En función del método de serialización que elija, escriba un archivo de definición de módulo (DEF), compile y vincule todos los archivos generados por MIDL en un único archivo DLL de proxy y registre la interfaz en el registro del sistema o registre la biblioteca de tipos. Vea [Cargar y registrar una biblioteca de tipos](loading-and-registering-a-type-library.md) y Compilar y registrar un archivo DLL de [proxy](building-and-registering-a-proxy-dll.md) para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anatomía de un archivo IDL](anatomy-of-an-idl-file.md)
</dt> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Reglas de diseño de interfaz](interface-design-rules.md)
</dt> <dt>

[The Component Object Model](the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> </dl>

 

 