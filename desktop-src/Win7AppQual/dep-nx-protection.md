---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protección de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913373"
---
# <a name="depnx-protection"></a>Protección de DEP/NX

A partir de Windows Internet Explorer 7 en Windows Vista, el elemento del panel de control de Internet incluye una opción **Habilitar protección de memoria** para ayudar a mitigar los ataques en línea. Esta opción también se conoce como *prevención de ejecución de datos* (DEP) o *no ejecutar* (NX). Cuando esta opción está habilitada, funciona con el procesador para ayudar a evitar ataques por desbordamiento del búfer al bloquear la ejecución del código de la memoria marcada como no ejecutable.

En Windows Internet Explorer 8 en el sistema operativo Windows Vista con Service Pack 1 (SP1) o una versión posterior, esta opción está habilitada de forma predeterminada. DEP/NX no protege contra todas las vulnerabilidades basadas en memoria. Sin embargo, cuando se combina con otras tecnologías, como la selección aleatoria del diseño del espacio de direcciones (ASLR), ayuda a evitar vulnerabilidades de desbordamiento de búfer comunes en Windows Internet Explorer y en los complementos que se cargan. No se requiere ninguna interacción del usuario adicional para proporcionar esta protección y no se introducen nuevos mensajes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



