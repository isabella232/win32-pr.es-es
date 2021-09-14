---
description: Configuración de la directiva de restricción de software
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configuración de la directiva de restricción de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965176"
---
# <a name="configuring-the-software-restriction-policy"></a>Configuración de la directiva de restricción de software

Cuando se establecen explícitamente los niveles de confianza de directiva de restricción de software de una aplicación COM+, se reemplaza la configuración predeterminada de todo el sistema. Esto suele ser necesario para las aplicaciones de servidor COM+ porque el nivel de confianza de todo el sistema se establece igual para todas las aplicaciones de servidor (porque todas se ejecutan en el mismo archivo, dllhost.exe). Sin embargo, cuando se establece el nivel de confianza de directiva de restricción de software de una aplicación de biblioteca COM+, se está afectando a la configuración de todo el sistema para esa aplicación. Para obtener una explicación sobre cómo usar la directiva de restricción de software en COM+, consulte Uso de [la directiva de restricción de software en COM+.](using-the-software-restriction-policy-in-com-.md)

**Para establecer la directiva de restricción de software**

1.  Haga clic con el botón derecho en la aplicación COM+ para la que va a establecer la directiva de restricción de software y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo propiedades de la aplicación, haga clic en **la pestaña** Seguridad .

3.  En **Directiva de restricción de software,** active la casilla Aplicar directiva de **restricción** de software; esto le permite establecer el nivel de confianza. Al desactivar la casilla, COM+ usará la configuración de todo el sistema de la directiva de restricción de software para la aplicación. Esta casilla corresponde a la propiedad SRPEnabled de la [**colección Applications.**](applications.md)

4.  En el **cuadro Nivel de** restricción, seleccione el nivel adecuado. Este cuadro desplegable corresponde a la propiedad SRPTrustLevel de la [**colección Applications.**](applications.md) Los niveles son los siguientes, ordenados de menos a más de confianza:

    -   **No permitido.** No se permite que la aplicación use los privilegios completos del usuario. Los componentes con cualquier nivel de confianza se pueden cargar en él.
    -   **Sin restricciones.** La aplicación tiene acceso sin restricciones a los privilegios del usuario. Solo se pueden cargar en él los componentes con un nivel de confianza sin restricciones.

5.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Role-Based seguridad](configuring-role-based-security.md)
</dt> <dt>

[Habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Establecer un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[Establecer un nivel de suplantación](setting-an-impersonation-level.md)
</dt> </dl>

 

 



