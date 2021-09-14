---
description: La realización de este paso permite procesar las comprobaciones de acceso o la seguridad completa basada en roles, en función del nivel de seguridad que seleccione y de si habilita la comprobación de acceso para componentes individuales.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Habilitar comprobaciones de acceso para una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240885"
---
# <a name="enabling-access-checks-for-an-application"></a>Habilitar comprobaciones de acceso para una aplicación

La realización de este paso permite procesar las comprobaciones de acceso o la seguridad completa basada en roles, en función del nivel de seguridad que seleccione y de si habilita la comprobación de acceso para componentes individuales.

**Para habilitar las comprobaciones de acceso de una aplicación**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en la aplicación COM+ para la que desea habilitar las comprobaciones de acceso y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo propiedades de la aplicación, haga clic en **la pestaña** Seguridad.

3.  Active la **casilla Aplicar comprobaciones de acceso para esta** aplicación.

4.  Haga clic en **OK**.

> [!Note]  
> A partir Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+. Las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente. Anteriormente, las comprobaciones de acceso se deshabilitaban de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente.

 

Después de habilitar las comprobaciones de acceso, debe seleccionar el nivel de seguridad adecuado. Vea [Establecer un nivel de seguridad para las comprobaciones de acceso.](setting-a-security-level-for-access-checks.md) Además, debe asegurarse de definir roles y agregarlos a la aplicación. Si las comprobaciones de acceso están habilitadas pero no se han agregado roles, se producirá un error en todas las llamadas a la aplicación. Consulte [Definición de roles para una aplicación.](defining-roles-for-an-application.md)

> [!Note]  
> Al depurar la aplicación, puede resultar útil deshabilitar la seguridad para que pueda concentrarse en otros aspectos del comportamiento y el diseño del programa.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de Role-Based seguridad](configuring-role-based-security.md)
</dt> <dt>

[Definir roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Establecer un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



