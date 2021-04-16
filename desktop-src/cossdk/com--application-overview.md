---
description: Una aplicación COM+ es la unidad principal de administración y seguridad para servicios de componentes y consta de un grupo de componentes COM que, por lo general, realizan funciones relacionadas.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Información general de la aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105670047"
---
# <a name="com-application-overview"></a>Información general de la aplicación COM+

Una aplicación COM+ es la unidad principal de administración y seguridad para servicios de componentes y consta de un grupo de componentes COM que, por lo general, realizan funciones relacionadas. Estos componentes se componen además de interfaces y métodos, tal y como se muestra en la siguiente ilustración.

![Diagrama que muestra las interfaces y los métodos dentro de los cuadros, en el orden del método dentro de la interfaz dentro del componente dentro de la aplicación COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

Puede usar la herramienta administrativa Servicios de componentes para crear nuevas aplicaciones COM+, agregar componentes a las aplicaciones y establecer los atributos de una aplicación y sus componentes.

Al crear grupos lógicos de componentes COM como aplicaciones COM+, puede aprovechar las ventajas de COM+ siguientes:

-   Un ámbito de implementación para los componentes COM.
-   Un ámbito de configuración común para los componentes COM, incluidos los límites de seguridad y la puesta en cola.
-   Almacenamiento de atributos de componentes no proporcionados por el desarrollador de componentes (por ejemplo, transacciones y sincronización).
-   Bibliotecas de vínculos dinámicos (dll) de componentes cargadas en procesos (DLLHost.exe) a petición.
-   Procesos de servidor administrados para hospedar componentes de.
-   Creación y administración de subprocesos utilizados por los componentes de.
-   Acceso al objeto de contexto para los distribuidores de recursos, permitiendo que los recursos adquiridos se asocien automáticamente al contexto. (Para obtener más información sobre los componentes y contextos COM, vea [contextos com+](com--contexts.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones COM+](developing-com--applications.md)
</dt> <dt>

[Partes de una aplicación COM+](parts-of-a-com--application.md)
</dt> <dt>

[Tipos de aplicaciones COM+](types-of-com--applications.md)
</dt> </dl>

 

 



