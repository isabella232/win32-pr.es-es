---
title: Carga del carácter predeterminado
description: Carga del carácter predeterminado
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f99d194843c6196f69e287857ce08097e849f328738c5f5d1a6e7feba0c53d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247612"
---
# <a name="loading-the-default-character"></a>Carga del carácter predeterminado

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

En lugar de cargar solo un carácter específico directamente especificando su nombre de archivo, puede cargar el *carácter predeterminado*. El carácter predeterminado es un servicio diseñado para proporcionar un asistente de Windows compartido que el usuario elija. Microsoft Agent incluye una hoja de propiedades como parte del servicio de caracteres predeterminado, conocido como character ventana Propiedades, que permite al usuario cambiar su selección del carácter predeterminado.

La selección del carácter predeterminado se limita a un carácter que admite el conjunto de animaciones estándar, lo que garantiza un nivel básico de coherencia entre caracteres. Esto no excluye que un carácter tenga animaciones adicionales.

Sin embargo, dado que el carácter predeterminado está pensado para uso general y puede ser compartido por otras aplicaciones al mismo tiempo, evite cargar el carácter predeterminado cuando desee un carácter exclusivamente para la aplicación.

Para cargar el carácter predeterminado, llame al [**método Load**](load-method.md) sin especificar un nombre de archivo o una ruta de acceso. Microsoft Agent carga automáticamente el juego de caracteres actual como carácter predeterminado. Si el usuario aún no ha seleccionado un carácter predeterminado, el Agente seleccionará el primer carácter que admita el conjunto de animaciones estándar. Si no hay ninguna disponible, el método producirá un error e informará de la causa.

Aunque una aplicación cliente puede preguntar sobre la identidad del carácter, solo un usuario puede cambiar su configuración. Puede usar [**ShowDefaultCharacterProperties para**](showdefaultcharacterproperties-method.md) mostrar el carácter ventana Propiedades.

El servidor notificará a los clientes que han cargado el carácter predeterminado cuando un usuario cambia una selección de caracteres y pasa el GUID del nuevo carácter. El servidor descarga automáticamente el carácter anterior y vuelve a cargar el nuevo carácter. Las colas de los clientes que han cargado el carácter predeterminado se detienen y vacían. Sin embargo, las colas de clientes que han cargado el carácter explícitamente mediante el nombre de archivo del carácter no se ven afectadas. Si es necesario, el servidor también controla el restablecimiento automático del motor de texto a voz (TTS) para el nuevo carácter.

 

 




