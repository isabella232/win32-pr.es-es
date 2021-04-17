---
description: Al realizar este paso, se habilitan las comprobaciones de acceso al proceso o la seguridad basada en roles completa, según el nivel de seguridad que seleccione y si habilita la comprobación de acceso para componentes individuales.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Habilitación de las comprobaciones de acceso para una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696104"
---
# <a name="enabling-access-checks-for-an-application"></a>Habilitación de las comprobaciones de acceso para una aplicación

Al realizar este paso, se habilitan las comprobaciones de acceso al proceso o la seguridad basada en roles completa, según el nivel de seguridad que seleccione y si habilita la comprobación de acceso para componentes individuales.

**Para habilitar las comprobaciones de acceso para una aplicación**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en la aplicación COM+ para la que desea habilitar las comprobaciones de acceso y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .

3.  Active la casilla **exigir comprobaciones de acceso para esta aplicación** .

4.  Haga clic en **OK**.

> [!Note]  
> A partir de Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+. Las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente. Anteriormente, las comprobaciones de acceso estaban deshabilitadas de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente.

 

Después de habilitar las comprobaciones de acceso, debe seleccionar el nivel de seguridad adecuado. Consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md). Además, debe asegurarse de definir roles y agregarlos a la aplicación. Si se habilitan las comprobaciones de acceso pero no se ha agregado ningún rol, se producirá un error en todas las llamadas a la aplicación. Consulte [definición de roles para una aplicación](defining-roles-for-an-application.md).

> [!Note]  
> Al depurar la aplicación, puede resultar útil deshabilitar la seguridad para que pueda concentrarse en otros aspectos del diseño y el comportamiento de su programa.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de la seguridad de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definición de roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Establecimiento de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



