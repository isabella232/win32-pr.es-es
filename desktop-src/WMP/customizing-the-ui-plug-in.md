---
title: Personalizar el complemento de la interfaz de usuario
description: Personalizar el complemento de la interfaz de usuario
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Complementos de Windows Media Player, personalizar
- complementos, personalizar
- Complementos de la interfaz de usuario, personalizar
- Complementos de la interfaz de usuario, personalizar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076131"
---
# <a name="customizing-the-ui-plug-in"></a>Personalizar el complemento de la interfaz de usuario

En este momento, el proyecto está listo para la personalización. Puede modificar la implementación generada por el Asistente de la interfaz **IWMPPluginUI** , puede Agregar una interfaz de usuario a la clase **CPluginWindow** y puede implementar una página de propiedades en la clase **CPropertyDialog** . Si el complemento está configurado para escuchar eventos de Media Player de Windows, el asistente habrá generado implementaciones predeterminadas o vacías de todos los controladores de eventos necesarios, que también se modifican o se crean.

El tipo de complemento y las características que admite se indican mediante un valor que se almacena en el registro de Windows. El asistente genera un archivo con la extensión de nombre de archivo. RGS que contiene la información para registrar el complemento. El valor "Capabilities" de este archivo es el equivalente decimal de un booleano o de las constantes de tipo de complemento y las marcas de complemento definidas en wmpplug. h. Aunque este valor está determinado por las opciones que seleccione en el asistente, debe modificarlo Si desea crear un complemento con varios valores preestablecidos o uno al que se puedan enviar los elementos multimedia o listas de reproducción.

A medida que modifica y extiende el código de complemento, puede compilar y registrar el archivo DLL para que pueda probar el complemento en Windows Media Player.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Compilar un complemento de IU**](building-a-ui-plug-in.md)
</dt> </dl>

 

 




