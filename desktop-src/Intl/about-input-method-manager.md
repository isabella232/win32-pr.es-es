---
description: El uso de la funcionalidad de IMM en la aplicación compatible con IME libera a los usuarios de la necesidad de recordar todos los valores de caracteres posibles.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Acerca del administrador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687834"
---
# <a name="about-input-method-manager"></a>Acerca del administrador de métodos de entrada

El uso de la funcionalidad de IMM en la aplicación compatible con IME libera a los usuarios de la necesidad de recordar todos los valores de caracteres posibles. En su lugar, permite que el IME supervise las pulsaciones de teclas de un usuario, prevea los caracteres que el usuario podría querer y presenta una lista de caracteres candidatos entre los que elegir.

> [!Note]  
> El IMM realiza operaciones similares a las del [marco de trabajo de servicios de texto](../tsf/text-services-framework.md), usadas por las aplicaciones que se comunican con los servicios de texto.

 

De forma predeterminada, el IMM proporciona una ventana IME a través de la cual el usuario introduce pulsaciones de teclas y vistas y selecciona candidatos. Las aplicaciones pueden usar las funciones y los mensajes de IMM para crear y administrar sus propias ventanas de IME, proporcionando una interfaz personalizada mientras usa las capacidades de conversión del IME.

El IMM solo está habilitado en los sistemas operativos de Windows localizados de Asia Oriental (Chino, Japonés, Coreano). En estos sistemas, la aplicación llama a [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ DBCSENABLED para determinar si el IMM está habilitado.

**Windows 2000:** La compatibilidad con el IMM completo se proporciona en todas las versiones de idioma localizadas. Sin embargo, el IMM solo está habilitado cuando se instala un paquete de idioma asiático. Una aplicación compatible con IME puede llamar a [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ IMMENABLED para determinar si el IMM está habilitado.

En este tema se incluyen las siguientes secciones.

-   [Listas de candidatos](candidate-lists.md)
-   [Cadena de composición](composition-string.md)
-   [HexToUnicode IME](hextounicode-ime.md)
-   [Hot Keys](hot-keys.md)
-   [Mensajes IME](ime-messages.md)
-   [Clase de ventana IME](ime-window-class.md)
-   [Contexto de entrada](input-context.md)
-   [Ventanas de estado, composición y candidatos](status--composition--and-candidates-windows.md)

 

 
