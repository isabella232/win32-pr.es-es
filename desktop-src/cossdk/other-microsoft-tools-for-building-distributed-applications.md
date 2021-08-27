---
description: Otras herramientas de Microsoft para compilar aplicaciones distribuidas
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Otras herramientas de Microsoft para compilar aplicaciones distribuidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9114454dbbeaa3c8f21cc1ea5166f93760fdd99772425f0245d7b8883f2db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070405"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Otras herramientas de Microsoft para compilar aplicaciones distribuidas

Además de las herramientas de COM+, Microsoft proporciona las siguientes herramientas para ayudar al desarrollador a crear aplicaciones distribuidas:

-   Microsoft Data Access Components (MDAC). Microsoft proporciona varias vías para recuperar datos de una gran cantidad de orígenes. Por ejemplo, OLE DB ofrece un conjunto de interfaces COM para compilar componentes de base de datos. Las interfaces se definen para que los proveedores de datos puedan implementar diferentes niveles de compatibilidad, en función de las funcionalidades del almacén de datos subyacente. Dado OLE DB está basado en COM, se puede ampliar fácilmente y las extensiones se implementan como nuevas interfaces. OLE DB también incluye una interfaz de programación de nivel de aplicación, denominada ActiveX Data Objects (ADO). ADO expone interfaces duales, por lo que se puede usar fácilmente desde lenguajes de scripting, así como Microsoft Visual C++, Visual Basic y otras herramientas para desarrolladores.

    > [!Note]  
    > Los desarrolladores también pueden optar por usar una API genérica neutral para el proveedor, como la interfaz de programación de aplicaciones (API) microsoft Open Database Connectivity (ODBC). La API de ODBC es una interfaz del lenguaje C para acceder a los datos de un DBMS mediante Lenguaje de consulta estructurado (SQL). Un administrador de controladores ODBC proporciona la interfaz de programación y los componentes en tiempo de ejecución para buscar controladores específicos de DBMS. Los controladores ODBC, normalmente proporcionados por el proveedor de DBMS, traducen las llamadas genéricas del administrador de controladores ODBC en llamadas al método de acceso a datos nativos. La principal ventaja de usar la API de ODBC es que solo necesita aprender una API para acceder a una amplia gama de DBMS.

     

-   Microsoft SQL Server. Además de proporcionar un sistema de base de datos relacional sólido y elocuente, Microsoft SQL Server puede proporcionar una aplicación distribuida con la agrupación de conexiones y la seguridad que se pueden integrar con el modelo de seguridad de Windows.

-   Integración de transacciones COM (COMTI). COMTI se puede usar para integrar sistemas centrales en sistemas Windows, incluidas las aplicaciones COM+. COMTI usa protocolos de comunicación estándar (por ejemplo, LU 6.2) para la comunicación entre Windows equipos y sistemas centrales y miniequipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suposiciones y principios de diseño de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Diseño de la aplicación COM+ mediante UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Diseño general Sugerencias para usar COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimización de interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



