---
description: Tanto si decide convertir los paquetes MTS en aplicaciones COM+ manualmente como si deja que el proceso de instalación de Microsoft Windows lo haga automáticamente, debe tener en cuenta los resultados de la conversión, así como los problemas.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Resultados y problemas de conversión de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465568"
---
# <a name="com-conversion-results-and-issues"></a>Resultados y problemas de conversión de COM+

Tanto si decide convertir los paquetes MTS en aplicaciones COM+ manualmente como si deja que el proceso de instalación de Microsoft Windows lo haga automáticamente, debe tener en cuenta los resultados de la conversión, así como los problemas.

## <a name="what-is-converted"></a>¿Qué se convierte?

Durante la conversión, la utilidad MTSTOCOM convierte roles, asignaciones de roles, interfaces, métodos, usuarios, la lista de equipos y la mayoría de la configuración del equipo. La utilidad MTSTOCOM también convierte la identidad y la contraseña de un paquete MTS.

Los nuevos atributos COM+ que no estaban disponibles en MTS se establecen automáticamente en los siguientes valores predeterminados para todos los componentes de MTS convertidos. Estos valores predeterminados se pueden cambiar mediante la herramienta administrativa Servicios de componentes o las interfaces administrativas de COM+.

-   Activación JIT habilitada.
-   Agrupación de objetos deshabilitada.
-   Sincronización igual que la configuración de transacción.

## <a name="conversion-issues"></a>Problemas de conversión

COM+ se instala automáticamente al instalar Windows. No es posible desinstalar COM+. Entre los problemas relacionados con las actualizaciones de las instalaciones de MTS y COM+ existentes se incluyen los siguientes:

-   Si actualmente usa MTS 1.0, MTS se actualiza automáticamente a COM+. Sin embargo, los paquetes definidos por el usuario se perderán y debe volver a crearlos.
-   Si actualmente usa MTS 2.0, MTS se actualiza automáticamente a COM+. Todos los paquetes definidos por el usuario se actualizarán a aplicaciones COM+. Todos los componentes deben funcionar como lo hacían en MTS 2.0.
-   Si usa MTS 1.0 y MTS 2.0 y ha instalado la opción SDK, se quitarán los archivos del SDK. Puede instalar el SDK de COM+ más reciente a través del SDK Windows Microsoft.
-   No se puede administrar un equipo MTS remoto desde un equipo COM+.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conversión automática desde MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Conversión manual desde MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de administración de MTS](mts-administration-library.md)
</dt> </dl>

 

 



