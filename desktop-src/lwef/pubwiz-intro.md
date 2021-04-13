---
title: Introducción a los asistentes para publicación
description: Windows XP presenta el Asistente para publicación web y el Asistente para la ordenación de impresión en línea.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- asistentes para la publicación, acerca de
- Asistente para publicación Web, acerca de
- Asistente para orden de impresión en línea, acerca de
- asistentes para publicación, Asistente para publicación Web
- asistentes para publicación, Asistente para impresión en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b4e6d3c515edae23d0e74f550e000bdfdfacf03
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487562"
---
# <a name="publishing-wizards-introduction"></a>Introducción a los asistentes para publicación

Windows XP presenta el Asistente para publicación web y el Asistente para la ordenación de impresión en línea. En función del mismo marco de trabajo, estos asistentes proporcionan al usuario un mecanismo sencillo para publicar contenido en un sitio web o para ordenar las impresiones realizadas a partir de archivos de imágenes digitales. La ventaja de estos asistentes radica en su capacidad para hospedar contenido HTML de distintos proveedores dentro de las páginas del asistente, de modo que las opciones buscar, procedimiento y usuario disponible estén controladas por completo por el proveedor y se puedan modificar en cualquier momento sin que ello afecte al asistente del cliente que los hospeda. Aunque estos asistentes existentes se han creado pensando en la creación de imágenes digitales, el marco y los conceptos se pueden usar para muchos otros fines, como un servicio de impresión de documentos o como método para compartir imágenes con amigos y familiares.

-   [¿Cómo funciona?](#how-does-it-work)
-   [Documentación del Asistente para publicación](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>¿Cómo funciona?

La experiencia del usuario para el Asistente para publicación web y el Asistente para la ordenación de impresión en línea es similar, pero el punto de entrada de cada asistente es diferente. En el Asistente para publicación Web, una tarea titulada **publicar esta carpeta en Web** está disponible en la lista de **tareas de archivos y carpetas** a la izquierda de la mayoría de las vistas de carpeta. El texto de la tarea varía en función del contenido seleccionado. Por ejemplo, si se selecciona un archivo, la tarea Lee **publicar este archivo en la web** , tal como se muestra en el ejemplo siguiente.

![tareas de archivos y carpetas](images/shell-pubwiz-tasks.png)

El usuario hace clic en la tarea para iniciar el asistente. Al continuar con el asistente, se muestra al usuario una lista de proveedores, tal como se muestra en el ejemplo siguiente. Los proveedores de servicios Internet (ISP) pueden desarrollar y registrar sus propias páginas de proveedor para que se muestren en esta lista.

![lista de proveedores del Asistente para publicación](images/shell-pubwiz-provs.png)

Una vez que se elige un proveedor, el asistente se conecta a ese sitio y se descarga la primera página HTML para su presentación en el asistente. Si los usuarios no tienen una cuenta con el proveedor seleccionado, se les da la oportunidad de configurar uno.

Varias páginas HTML están contenidas en una sola página del asistente; en otras palabras, el identificador de la página del asistente que hospeda el procesamiento de páginas HTML permanece constante. Las páginas HTML se exponen en el panel central como con cualquier página del asistente estándar. El sitio del proveedor proporciona métodos para controlar el lugar en el que se muestran los botones **atrás**, **siguiente** y **Cancelar** del asistente mientras se muestran las páginas HTML. Dentro de esas páginas HTML, es posible que se pida a los usuarios que especifiquen una carpeta donde puedan copiar archivos o guardar el nombre de un sitio web que deseen crear. Una vez que un usuario ha completado todos los pasos necesarios, el sitio llama a un método para comenzar la carga y devuelve el control al asistente. El propio asistente controla la carga y los gráficos del operador, como un indicador de progreso. Una vez completada la carga, el sitio del proveedor puede especificar una dirección URL en la que el usuario puede ir una vez que el asistente se ha cerrado.

En el Asistente para orden de impresión en línea, el orden de las tareas **copias de seguridad en línea** solo se ve en carpetas de imágenes como mis imágenes, que se muestra en el ejemplo siguiente. El proceso, sin embargo, es muy similar al Asistente para publicación en Web. El sitio del proveedor solicita a los usuarios opciones como la selección de imágenes, tamaños de impresión, número de copias e información de pago.

![tareas de imagen](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Documentación del Asistente para publicación

El Asistente para publicación web y el Asistente para la ordenación de impresión en línea se describen en detalle en los siguientes documentos. También se describen las instrucciones para desarrollar aplicaciones que se van a hospedar en ellas.

-   [Diseño del lado cliente](pubwiz-client.md)
-   [Diseño del lado servidor](pubwiz-server.md)
-   [Registrar un servicio](pubwiz-reg.md)
-   [Usar el manifiesto de transferencia](pubwiz-manifest.md)
-   [Transferir esquema de manifiesto](/windows/desktop/shell/interfaces)

 

 