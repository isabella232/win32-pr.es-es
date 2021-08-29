---
title: Selección del motor de voz
description: Selección del motor de voz
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3998817e5eba041b1fb20eb9df64ee26217da974ff4d91869af05fbf15cc4f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960965"
---
# <a name="speech-engine-selection"></a>Selección del motor de voz

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

La configuración del identificador de idioma de un carácter determina su idioma de entrada de voz predeterminado; Microsoft Agent solicita SAPI para un motor instalado que coincida con ese idioma. Si una aplicación cliente no especifica una preferencia de idioma, Microsoft Agent intentará encontrar un motor de reconocimiento de voz que coincida con el identificador de idioma predeterminado del usuario (mediante el identificador de idioma principal y, a continuación, el identificador de idioma menor). Si no hay ningún motor disponible que coincida con este idioma, la voz se deshabilita para ese carácter.

También puede solicitar un motor de reconocimiento de voz específico especificando su identificador de modo (mediante la [**propiedad SRModeID del**](srmodeid-property.md) carácter). Sin embargo, si el identificador de idioma de ese identificador de modo no coincide con la configuración de idioma del cliente, se producirá un error en la llamada (se producirá un error en el control ). A continuación, el motor de reconocimiento de voz seguirá siendo el último motor configurado correctamente por el cliente o, si no lo hay, el motor que coincida con el identificador de idioma del sistema actual. Si todavía no hay ninguna coincidencia, la entrada de voz no está disponible para ese cliente.

Microsoft Agent carga automáticamente un motor de reconocimiento de voz cuando un usuario inicia la entrada de voz presionando la tecla de acceso rápido Escucha o el cliente activo de entrada llama al [**método Listen.**](listen-method.md) Sin embargo, también se puede cargar un motor al establecer o consultar su identificador de modo, establecer o consultar las propiedades de la ventana Comandos de voz, consultar [**SRStatus**](srstatus-property.md)o cuando la voz está habilitada y el usuario muestra la página Entrada de voz de opciones avanzadas de caracteres. Sin embargo, Microsoft Agent solo mantiene cargados los motores de voz que usan los clientes.

 

 




