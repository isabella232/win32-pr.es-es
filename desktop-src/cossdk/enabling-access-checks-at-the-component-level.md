---
description: Habilitar comprobaciones de acceso en el nivel de componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Habilitar comprobaciones de acceso en el nivel de componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705264"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Habilitar comprobaciones de acceso en el nivel de componente

Si la aplicación incluye un componente que no necesita comprobaciones de seguridad, puede decidir deshabilitar las comprobaciones de roles para ese componente con el fin de mejorar el rendimiento. O bien, al depurar, puede resultar útil deshabilitar la seguridad para que pueda concentrarse en otros aspectos de la funcionalidad del programa.

De forma predeterminada, cuando se instala un componente, se habilitan las comprobaciones de acceso de nivel de componente. Sin embargo, esto solo surte efecto cuando se habilitan las [comprobaciones de acceso de nivel de aplicación](enabling-access-checks-for-an-application.md) y cuando el [nivel de seguridad](setting-a-security-level-for-access-checks.md) se establece para **realizar comprobaciones de acceso en el nivel de proceso y de componente**.

**Para habilitar o deshabilitar las comprobaciones de acceso en el nivel de componente**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el componente para el que desea deshabilitar o habilitar las comprobaciones de rol. Expanda la vista en el árbol para ver los componentes en la carpeta **componentes** .

2.  Haga clic con el botón secundario en el componente para el que desea habilitar las comprobaciones de roles y, a continuación, haga clic en **propiedades**.

3.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **seguridad** .

4.  Seleccione **aplicar comprobaciones de acceso de nivel de componente** para aplicar comprobaciones de nivel de componente.

5.  Haga clic en **OK**.

La nueva configuración surtirá efecto la próxima vez que se inicie la aplicación.

> [!Note]  
> A partir de Windows Server 2003, las comprobaciones de acceso de nivel de componente están deshabilitadas de forma predeterminada al crear una aplicación COM+. Las comprobaciones de acceso están habilitadas de forma predeterminada en el nivel de aplicación y deshabilitadas de forma predeterminada en el nivel de componente. Anteriormente, las comprobaciones de acceso estaban deshabilitadas de forma predeterminada en el nivel de aplicación y se habilitaban de forma predeterminada en el nivel de componente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de la seguridad de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definición de roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitación de las comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Establecimiento de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



