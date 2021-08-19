---
description: Protección de DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protección de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec30b3758361cbe2ed20e67fe6792d6f76b58a7266c6de1d554afdba8a2519c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329945"
---
# <a name="depnx-protection"></a>Protección de DEP/NX

A partir de Windows Internet Explorer 7 en Windows Vista, el elemento del panel de control de Internet incluye una opción Habilitar protección de memoria para ayudar **a** mitigar los ataques en línea. Esta opción también se conoce como *Prevención de ejecución* de datos (DEP) *o No-Execute* (NX). Cuando esta opción está habilitada, funciona con el procesador para ayudar a evitar ataques de desbordamiento de búfer bloqueando la ejecución de código desde la memoria marcada como no ejecutable.

En Windows Internet Explorer 8 en Windows Vista con el sistema operativo Service Pack 1 (SP1) o una versión posterior, esta opción está habilitada de forma predeterminada. DEP/NX no protege contra todas las vulnerabilidades basadas en memoria. Pero cuando se combina con otras tecnologías como la selección aleatoria del diseño del espacio de direcciones (ASLR), ayuda a evitar vulnerabilidades comunes de desbordamiento de búfer en Windows Internet Explorer y los complementos que carga. No se requiere ninguna interacción adicional del usuario para proporcionar esta protección y no se introducen nuevos avisos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



