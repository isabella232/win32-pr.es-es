---
title: Opciones del complemento de interfaz de usuario
description: Opciones del complemento de interfaz de usuario
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Reproductor de Windows Media complementos,opciones
- complementos, opciones
- complementos de interfaz de usuario, opciones
- Complementos de interfaz de usuario, opciones
- complementos del área de configuración
- complementos de fondo
- complementos de ventana independientes
- complementos del área de metadatos
- complementos de área de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465809"
---
# <a name="ui-plug-in-options"></a>Opciones del complemento de interfaz de usuario

Cualquiera de los cinco tipos de complemento de interfaz de usuario puede tener una página de propiedades donde el usuario puede modificar la configuración del complemento. Esta página de propiedades se puede establecer para mostrarse automáticamente cuando se carga un complemento por primera vez. También se puede acceder a él desde la pestaña Complementos del cuadro de diálogo Opciones .

Un complemento de interfaz de usuario se puede establecer para cargarse automáticamente después de la instalación Reproductor de Windows Media se inicia. Si no se inicia automáticamente, el usuario puede cargarlo  seleccionándose en la lista Complementos del **menú** Herramientas.

Un complemento de área de presentación puede tener varios valores preestablecidos, que son vistas diferentes que el complemento puede hacer que estén disponibles para el usuario. El usuario puede cambiar el valor preestablecido seleccionando una entrada  diferente en la lista Visualizaciones y vistas  del menú Ver o mediante los **botones** de flecha que se proporcionan en la parte inferior del panel Reproducción ahora justo encima del mensaje de estado y los controles de transporte.

Se pueden programar complementos de interfaz de usuario de ventana independientes y en segundo plano para aceptar un elemento multimedia o una lista de reproducción que el usuario le envíe. Si un complemento admite esta característica, su  nombre aparecerá en la lista Enviar a disponible en el menú contextual del control de lista de reproducción o la biblioteca.

Un complemento de interfaz de usuario se puede programar para interceptar métodos abreviados de teclado cuando tiene el foco de teclado. El foco de teclado es necesario para evitar conflictos cuando se cargan varios complementos de interfaz de usuario que interceptan el mismo método abreviado de teclado. Aunque esto evita conflictos, también puede causar confusión a los usuarios finales. Por este motivo, no se recomienda el uso de métodos abreviados de teclado con complementos de interfaz de usuario. Sin embargo, cuando se usan, no deben interceptar los métodos abreviados de teclado usados por Reproductor de Windows Media. Para obtener una lista completa de los métodos abreviados de teclado que usa el reproductor, consulte Reproductor de Windows Media Ayuda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general sobre el complemento de interfaz de usuario**](ui-plug-in-overview.md)
</dt> </dl>

 

 




