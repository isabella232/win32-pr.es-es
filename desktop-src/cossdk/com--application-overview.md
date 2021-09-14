---
description: Una aplicación COM+ es la unidad principal de administración y seguridad de servicios de componentes y consta de un grupo de componentes COM que generalmente realizan funciones relacionadas.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Introducción a la aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073006"
---
# <a name="com-application-overview"></a>Introducción a la aplicación COM+

Una aplicación COM+ es la unidad principal de administración y seguridad de servicios de componentes y consta de un grupo de componentes COM que generalmente realizan funciones relacionadas. Estos componentes constan además de interfaces y métodos, como se muestra en la ilustración siguiente.

![Diagrama que muestra interfaces y métodos dentro de cuadros, en orden de Método dentro de interfaz dentro de Componente dentro de la aplicación COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

Puede usar la herramienta administrativa Servicios de componentes para crear nuevas aplicaciones COM+, agregar componentes a las aplicaciones y establecer los atributos de una aplicación y sus componentes.

Al crear grupos lógicos de componentes COM como aplicaciones COM+, puede aprovechar las siguientes ventajas de COM+:

-   Ámbito de implementación para componentes COM.
-   Un ámbito de configuración común para los componentes COM, incluidos los límites de seguridad y la cola.
-   Storage atributos de componente no proporcionados por el desarrollador de componentes (por ejemplo, transacciones y sincronización).
-   Bibliotecas de vínculos dinámicos (DLL) de componentes cargadas en procesos (DLLHost.exe) a petición.
-   Procesos de servidor administrado para hospedar componentes.
-   Creación y administración de subprocesos usados por componentes.
-   Acceso al objeto de contexto para los distribuidores de recursos, lo que permite que los recursos adquiridos se asocie automáticamente al contexto. (Para obtener más información sobre los componentes y contextos COM, vea [Contextos COM+).](com--contexts.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones COM+](developing-com--applications.md)
</dt> <dt>

[Partes de una aplicación COM+](parts-of-a-com--application.md)
</dt> <dt>

[Tipos de aplicaciones COM+](types-of-com--applications.md)
</dt> </dl>

 

 



