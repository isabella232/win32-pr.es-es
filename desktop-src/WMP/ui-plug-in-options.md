---
title: Opciones del complemento de la interfaz de usuario
description: Opciones del complemento de la interfaz de usuario
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Complementos de Media Player de Windows, opciones
- complementos, opciones
- Complementos de la interfaz de usuario, opciones
- Complementos de la interfaz de usuario, opciones
- Complementos de área de configuración
- Complementos de fondo
- Complementos de ventana independientes
- Complementos de área de metadatos
- Complementos de área de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704599"
---
# <a name="ui-plug-in-options"></a>Opciones del complemento de la interfaz de usuario

Cualquiera de los cinco tipos de complementos de la interfaz de usuario puede tener una página de propiedades en la que el usuario puede modificar la configuración del complemento. Esta página de propiedades se puede establecer para que se muestre automáticamente cuando se carga un complemento por primera vez. También se puede obtener acceso a él desde la pestaña complementos del cuadro de diálogo Opciones.

Se puede configurar un complemento de la interfaz de usuario para que se cargue automáticamente después de la instalación cuando se inicie Windows Media Player. Si no se inicia automáticamente, el usuario puede cargarla seleccionándola en la lista de **Complementos** del menú **herramientas** .

Un complemento de área de presentación puede tener varios valores predeterminados, que son vistas diferentes que el complemento puede poner a disposición del usuario. El usuario puede cambiar el valor preestablecido seleccionando una entrada diferente de la lista **visualizaciones y vistas** en el menú **Ver** o mediante los botones de flecha proporcionados en la parte inferior del panel **reproducción en curso** justo encima del mensaje de estado y los controles de transporte.

Los complementos de la interfaz de usuario de ventana independiente y de fondo se pueden programar para que acepten un elemento multimedia o una lista de reproducción que el usuario le envíe. Si un complemento es compatible con esta característica, su nombre aparecerá en la lista **Enviar a** disponible en el menú contextual del control de lista de reproducción o de la biblioteca.

Un complemento de interfaz de usuario se puede programar para interceptar los métodos abreviados de teclado cuando tiene el foco de teclado. El foco de teclado es necesario para evitar conflictos cuando se cargan varios complementos de la interfaz de usuario que interceptan el mismo método abreviado de teclado. Aunque esto evita conflictos, también puede provocar confusión en los usuarios finales. Por esta razón, no se recomienda el uso de métodos abreviados de teclado con complementos de interfaz de usuario. Sin embargo, cuando se utilizan, no deben interceptar los métodos abreviados de teclado que se usan en Windows Media Player. Para obtener una lista completa de los métodos abreviados de teclado utilizados por el reproductor, consulte la ayuda de Windows Media Player.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general del complemento de la interfaz de usuario**](ui-plug-in-overview.md)
</dt> </dl>

 

 




