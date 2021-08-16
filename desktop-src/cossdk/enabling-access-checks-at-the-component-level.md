---
description: Habilitar comprobaciones de acceso en el nivel de componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Habilitar comprobaciones de acceso en el nivel de componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3063873923d3d4c491312ca4efccd9bcd665b46bf1bdfc882b69dbe4942757f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047473"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Habilitar comprobaciones de acceso en el nivel de componente

Si la aplicación incluye un componente que no necesita comprobaciones de seguridad, puede decidir deshabilitar las comprobaciones de roles para ese componente a fin de mejorar el rendimiento. O bien, al depurar, puede resultar útil deshabilitar la seguridad para que pueda concentrarse en otros aspectos de la funcionalidad del programa.

De forma predeterminada, al instalar un componente, se habilitan las comprobaciones de acceso de nivel de componente. Sin embargo, esto [](enabling-access-checks-for-an-application.md) solo surte efecto cuando se [](setting-a-security-level-for-access-checks.md) habilitan las comprobaciones de acceso de nivel de aplicación y cuando el nivel de seguridad se establece en Realizar comprobaciones de acceso en el nivel de **proceso y componente**.

**Para habilitar o deshabilitar las comprobaciones de acceso en el nivel de componente**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el componente para el que desea deshabilitar (o habilitar) las comprobaciones de roles. Expanda la vista en el árbol para ver los componentes en la **carpeta** Componentes.

2.  Haga clic con el botón derecho en el componente para el que desea habilitar las comprobaciones de roles y, a continuación, haga clic en **Propiedades**.

3.  En el cuadro de diálogo propiedades del componente, haga clic en **la pestaña** Seguridad .

4.  Seleccione **Aplicar comprobaciones de acceso de nivel de componente** para aplicar comprobaciones de nivel de componente.

5.  Haga clic en **Aceptar**.

La nueva configuración se aplica la próxima vez que se inicia la aplicación.

> [!Note]  
> A partir Windows Server 2003, las comprobaciones de acceso de nivel de componente están deshabilitadas de forma predeterminada al crear una aplicación COM+. Las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente. Anteriormente, las comprobaciones de acceso se deshabilitaban de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de Role-Based seguridad](configuring-role-based-security.md)
</dt> <dt>

[Definir roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Establecer un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



