---
description: Otras herramientas de Microsoft para compilar aplicaciones distribuidas
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Otras herramientas de Microsoft para compilar aplicaciones distribuidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714868"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Otras herramientas de Microsoft para compilar aplicaciones distribuidas

Además de las herramientas de COM+, Microsoft proporciona las siguientes herramientas para ayudar al desarrollador a crear aplicaciones distribuidas:

-   Microsoft Data Access Components (MDAC). Microsoft proporciona varias vías para recuperar datos de una gran cantidad de orígenes. Por ejemplo, OLE DB ofrece un conjunto de interfaces COM para compilar componentes de base de datos. Las interfaces se definen para que los proveedores de datos puedan implementar distintos niveles de compatibilidad, en función de las capacidades del almacén de datos subyacente. Dado que OLE DB se basa en COM, se puede extender fácilmente y las extensiones se implementan como interfaces nuevas. OLE DB también incluye una interfaz de programación de nivel de aplicación, denominada Objetos de datos ActiveX (ADO). ADO expone interfaces duales, por lo que se puede usar fácilmente desde lenguajes de scripting, así como Microsoft Visual C++, Visual Basic y otras herramientas de desarrollo.

    > [!Note]  
    > Los desarrolladores también pueden optar por usar una API genérica, independiente del proveedor, como la interfaz de programación de aplicaciones (API) de Microsoft Open Database Connectivity (ODBC). La API de ODBC es una interfaz de lenguaje C para tener acceso a los datos de un DBMS mediante Lenguaje de consulta estructurado (SQL). Un administrador de controladores ODBC proporciona la interfaz de programación y los componentes en tiempo de ejecución para localizar controladores específicos del DBMS. Los controladores ODBC, normalmente suministrados por el proveedor de DBMS, traducen las llamadas genéricas del administrador de controladores ODBC en llamadas al método de acceso a datos nativo. La principal ventaja de utilizar la API de ODBC es que necesita aprender solo una API para tener acceso a una amplia gama de DBMS.

     

-   Microsoft SQL Server. Además de proporcionar un sistema de base de datos relacional sólido y Eloquent, Microsoft SQL Server puede proporcionar una aplicación distribuida con agrupación de conexiones y seguridad que pueda integrarse con el modelo de seguridad de Windows.

-   Integración de transacciones COM (COMTI). COMTI se puede usar para integrar sistemas de gran sistema en sistemas Windows, incluidas las aplicaciones COM+. COMTI usa protocolos de comunicación estándar (por ejemplo, LU 6,2) para la comunicación entre equipos Windows y mainframe y minicomputers.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hipótesis y principios de diseño de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Diseñar la aplicación COM+ mediante UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Sugerencias de diseño generales para el uso de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimizar interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



