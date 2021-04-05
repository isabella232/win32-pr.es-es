---
description: Configuración de la Directiva de restricción de software
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configuración de la Directiva de restricción de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080269"
---
# <a name="configuring-the-software-restriction-policy"></a>Configuración de la Directiva de restricción de software

Cuando se establecen explícitamente los niveles de confianza de la Directiva de restricción de software de una aplicación COM+, se invalida la configuración predeterminada de todo el sistema. Esto suele ser necesario para las aplicaciones de servidor COM+, ya que el nivel de confianza de todo el sistema se establece en todas las aplicaciones de servidor (ya que todos se ejecutan en el mismo archivo, dllhost.exe). Sin embargo, al establecer el nivel de confianza de la Directiva de restricción de software de una aplicación de biblioteca COM+, afecta a la configuración de todo el sistema para esa aplicación. Para obtener una explicación de cómo usar la Directiva de restricción de software en COM+, consulte [usar la Directiva de restricción de software en com+](using-the-software-restriction-policy-in-com-.md).

**Para establecer la Directiva de restricción de software**

1.  Haga clic con el botón secundario en la aplicación COM+ para la que está configurando la Directiva de restricción de software y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .

3.  En **Directiva de restricción de software**, active la casilla **aplicar Directiva de restricción de software** ; Esto le permite establecer el nivel de confianza. Si desactiva la casilla, COM+ usará la configuración de todo el sistema de la Directiva de restricción de software para la aplicación. Esta casilla corresponde a la propiedad SRPEnabled de la colección de [**aplicaciones**](applications.md) .

4.  En el cuadro **nivel de restricción** , seleccione el nivel adecuado. Este cuadro desplegable corresponde a la propiedad SRPTrustLevel de la colección de [**aplicaciones**](applications.md) . Los niveles son los siguientes, ordenados de menor a mayor confianza:

    -   No **permitido**. No se permite que la aplicación use los privilegios completos del usuario. Los componentes con cualquier nivel de confianza pueden cargarse en él.
    -   **Sin restricciones**. La aplicación tiene acceso ilimitado a los privilegios del usuario. Solo se pueden cargar en él los componentes con un nivel de confianza no restringido.

5.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Habilitar la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Establecer un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[Establecer un nivel de suplantación](setting-an-impersonation-level.md)
</dt> </dl>

 

 



