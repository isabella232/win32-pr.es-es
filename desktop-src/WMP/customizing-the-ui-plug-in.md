---
title: Personalización del complemento de interfaz de usuario
description: Personalización del complemento de interfaz de usuario
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Reproductor de Windows Media complementos, personalización
- complementos, personalización
- complementos de interfaz de usuario, personalización
- Complementos de interfaz de usuario, personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258863"
---
# <a name="customizing-the-ui-plug-in"></a>Personalización del complemento de interfaz de usuario

En este momento, el proyecto está listo para la personalización. Puede modificar la implementación generada por el asistente de la interfaz **IWMPPluginUI,** puede agregar una interfaz de usuario a la **clase CPluginWindow** y puede implementar una página de propiedades en la **clase CPropertyDialog.** Si el complemento está configurado para escuchar eventos de Reproductor de Windows Media, el asistente habrá generado implementaciones predeterminadas o vacías de todos los controladores de eventos necesarios, que también se modifican o crean.

El tipo de complemento y las características que admite se indican mediante un valor que se almacena en Windows registro. El asistente genera un archivo con una extensión de nombre de archivo .rgs que contiene la información con la que se registra el complemento. El valor "Capabilities" de este archivo es el equivalente decimal de un or booleano de las constantes de tipo de complemento y las marcas de complemento definidas en wmpplug.h. Aunque este valor viene determinado por las opciones que seleccione en el asistente, debe modificarlo si desea crear un complemento con varios valores preestablecidos o uno al que se puedan enviar elementos multimedia o listas de reproducción.

A medida que modifica y extiende el código del complemento, puede compilar y registrar el archivo DLL para que pueda probar el complemento Reproductor de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un complemento de interfaz de usuario**](building-a-ui-plug-in.md)
</dt> </dl>

 

 




