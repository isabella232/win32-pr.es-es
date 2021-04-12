---
description: Tanto si decide convertir los paquetes MTS en aplicaciones COM+ manualmente como si desea que el proceso de instalación de Microsoft Windows lo haga automáticamente, debe tener en cuenta los resultados de la conversión, así como de los problemas.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Resultados y problemas de la conversión de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423503"
---
# <a name="com-conversion-results-and-issues"></a>Resultados y problemas de la conversión de COM+

Tanto si decide convertir los paquetes MTS en aplicaciones COM+ manualmente como si desea que el proceso de instalación de Microsoft Windows lo haga automáticamente, debe tener en cuenta los resultados de la conversión, así como de los problemas.

## <a name="what-is-converted"></a>Lo que se convierte

Durante la conversión, la utilidad MTSTOCOM convierte los roles, las asignaciones de roles, las interfaces, los métodos, los usuarios, la lista de equipos y la mayor parte de la configuración del equipo. La utilidad MTSTOCOM también convierte la identidad y la contraseña para un paquete MTS.

Los nuevos atributos COM+ que no estaban disponibles en MTS se establecen automáticamente en los siguientes valores predeterminados para todos los componentes de MTS convertidos. Estos valores predeterminados se pueden cambiar mediante la herramienta administrativa Servicios de componentes o las interfaces administrativas de COM+.

-   Activación JIT habilitada.
-   Agrupación de objetos deshabilitada.
-   La sincronización es igual que la configuración de la transacción.

## <a name="conversion-issues"></a>Problemas de conversión

COM+ se instala automáticamente al instalar Windows. No es posible desinstalar COM+. Entre los problemas relacionados con las actualizaciones de las instalaciones de MTS y COM+ existentes se incluyen los siguientes:

-   Si actualmente usa MTS 1,0, MTS se actualiza automáticamente a COM+. Sin embargo, los paquetes definidos por el usuario se perderán y deberá volver a crearlos.
-   Si actualmente usa MTS 2,0, MTS se actualiza automáticamente a COM+. Todos los paquetes definidos por el usuario se actualizarán a las aplicaciones COM+. Todos los componentes deben funcionar tal y como se encontraban en MTS 2,0.
-   Si usa MTS 1,0 y MTS 2,0 y ha instalado la opción SDK, se quitarán los archivos del SDK. Puede instalar el SDK de COM+ más reciente a través de la Microsoft Windows SDK.
-   No se puede administrar un equipo MTS remoto desde un equipo de COM+.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conversión automática desde MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Conversión manual desde MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de administración de MTS](mts-administration-library.md)
</dt> </dl>

 

 



