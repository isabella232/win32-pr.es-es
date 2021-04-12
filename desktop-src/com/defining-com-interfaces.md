---
title: Definición de interfaces COM
description: Microsoft define muchas interfaces COM. En la mayoría de los casos, puede reutilizar estas interfaces genéricas. Sin embargo, algunas aplicaciones tienen requisitos específicos que hacen que sea deseable o necesario definir sus propias interfaces de objeto.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516c02a2c337b2c76229094b0e42d75b44f65d16
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149654"
---
# <a name="defining-com-interfaces"></a>Definición de interfaces COM

Microsoft define muchas interfaces COM. En la mayoría de los casos, puede reutilizar estas interfaces genéricas. Sin embargo, algunas aplicaciones tienen requisitos específicos que hacen que sea deseable o necesario definir sus propias interfaces de objeto.

Todas las interfaces COM deben derivar, directa o indirectamente, de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Dentro de esa restricción, la interfaz personalizada puede admitir casi cualquier método o parámetro, incluidos los métodos asincrónicos. También puede generar una biblioteca de tipos para las interfaces personalizadas para que los clientes puedan tener acceso a la información sobre los métodos del objeto en tiempo de ejecución. Después de definir una interfaz, describirla en Lenguaje de definición de interfaz de Microsoft (MIDL), compilarla y registrarla, úsela como cualquier interfaz genérica. Con COM distribuido, los métodos de interfaz están disponibles tanto para los procesos remotos como para otros procesos del mismo equipo.

Por último, la creación de interfaces COM requiere un entorno de desarrollo que incluya un compilador de C/C++ y el compilador de Midl.exe.

Los pasos para crear una interfaz COM son los siguientes:

-   Decida cómo desea proporcionar compatibilidad con la serialización para la interfaz; con el cálculo de referencias controlado por la biblioteca de tipos o con un archivo DLL de proxy/código auxiliar. Incluso se deben calcular las referencias de las interfaces en proceso si se van a utilizar en límites de apartamento. Es una buena idea crear compatibilidad con el cálculo de referencias en cada interfaz COM, incluso si no cree que lo necesitará. Vea [serialización](interface-marshaling.md) de la interfaz para obtener más información.
-   Describir la interfaz o interfaces en un archivo de definición de interfaz (IDL). Además, puede especificar determinados aspectos locales de la interfaz en un archivo de configuración de la aplicación (ACF). Si utiliza el cálculo de referencias controlado por la biblioteca de tipos, agregue una instrucción de [**biblioteca**](/windows/desktop/Midl/library) que haga referencia a las interfaces para las que desea generar información de tipos.
-   Utilice el compilador MIDL para generar un archivo de biblioteca de tipos y un archivo de encabezado, o archivos de proxy/código auxiliar de lenguaje C, un archivo de identificador de interfaz, un archivo de datos DLL y un archivo de encabezado. Vea la [compilación de MIDL](midl-compilation.md) para obtener más información.
-   Dependiendo del método de cálculo de referencias que elija, escriba un archivo de definición de módulo (DEF), compile y vincule todos los archivos generados por MIDL en un solo archivo DLL de proxy, registre la interfaz en el registro del sistema o registre la biblioteca de tipos. Vea [cargar y registrar una biblioteca de tipos](loading-and-registering-a-type-library.md) y [generar y registrar un archivo dll de proxy](building-and-registering-a-proxy-dll.md) para obtener más información.

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

 

 