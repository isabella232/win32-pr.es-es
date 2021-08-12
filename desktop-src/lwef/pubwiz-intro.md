---
title: Introducción a los asistentes para publicación
description: Windows XP presenta el Asistente para publicación web y el Asistente para pedidos de impresión en línea.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- asistentes para publicación, acerca de
- Asistente para publicación web, acerca de
- Asistente para ordenación de impresión en línea, acerca de
- asistentes para publicación,Asistente para publicación web
- asistentes para publicación, Asistente para pedidos de impresión en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d576d04579847d2e65bbc59399d11689259f8e64823a3c3068cafad912ff8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246681"
---
# <a name="publishing-wizards-introduction"></a>Introducción a los asistentes para publicación

Windows XP presenta el Asistente para publicación web y el Asistente para pedidos de impresión en línea. En función del mismo marco, estos asistentes proporcionan al usuario un mecanismo sencillo para publicar contenido en un sitio web o para ordenar las copias impresas realizadas a partir de archivos de imagen digital. La ventaja de estos asistentes radica en su capacidad de hospedar contenido HTML de distintos proveedores dentro de sus páginas del asistente para que el proveedor controle completamente las opciones de apariencia, procedimiento y usuario disponibles y puedan modificarlas en cualquier momento sin que ello afecte al asistente de cliente que los hospeda. Aunque estos asistentes existentes se han creado con la creación de imágenes digitales en mente, el marco y los conceptos se pueden usar para muchos otros propósitos, como un servicio de impresión de documentos o como un método para compartir imágenes con amigos y familiares.

-   [¿Cómo funciona?](#how-does-it-work)
-   [Documentación del Asistente para publicación](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>¿Cómo funciona?

La experiencia del usuario para el Asistente para publicación web y el Asistente para pedidos de impresión en línea es similar, pero el punto de entrada de cada asistente difiere. Para el Asistente para publicación web, una tarea titulada Publicar  esta carpeta en la **Web** está disponible en la lista Tareas de archivos y carpetas a la izquierda de la mayoría de las vistas de carpeta. El texto de la tarea varía en función del contenido seleccionado. Por ejemplo, si se selecciona un archivo, la tarea lee Publicar este archivo en **la Web** como se muestra en el ejemplo siguiente.

![tareas de archivos y carpetas](images/shell-pubwiz-tasks.png)

El usuario hace clic en la tarea para iniciar el asistente. Al continuar con el asistente, se presenta al usuario una lista de proveedores, como se muestra en el ejemplo siguiente. Los proveedores de servicios de Internet (ISP) pueden desarrollar y registrar sus propias páginas de proveedor para que se muestren en esta lista.

![lista de proveedores del asistente para publicación](images/shell-pubwiz-provs.png)

Una vez elegido un proveedor, el asistente se conecta a ese sitio y la primera página HTML se descarga para mostrarse en el asistente. Si los usuarios no tienen una cuenta con el proveedor seleccionado, tienen la oportunidad de configurar una.

Hay varias páginas HTML dentro de una sola página del asistente; en otras palabras, el identificador de la página del asistente que hospeda esa procesión de páginas HTML sigue siendo constante. Las páginas HTML se exponen en el panel central como con cualquier página del asistente estándar. El sitio del proveedor proporciona métodos para controlar  dónde se muestran los botones **Atrás,** Siguiente y Cancelar del asistente mientras se muestran las páginas HTML. Dentro de esas páginas HTML, es posible que se pida a los usuarios que especifiquen una carpeta donde puedan copiar archivos o guardar el nombre de un sitio web que desean crear. Una vez que un usuario ha completado todos los pasos necesarios, el sitio llama a un método para comenzar la carga y devuelve el control al asistente. El propio asistente controla la carga y cualquier gráfico de asistencia, como un indicador de progreso. Una vez completada la carga, el sitio del proveedor puede especificar una dirección URL a la que el usuario pueda ir una vez cerrado el asistente.

En el Asistente para ordenación de impresión en línea, la tarea **Order prints online** solo se ve en carpetas de imágenes como Mis imágenes, que se muestra en el ejemplo siguiente. Sin embargo, el proceso es muy similar al Asistente para publicación web. El sitio del proveedor solicita a los usuarios opciones como la selección de imágenes, los tamaños de impresión, el número de copias y la información de pago.

![tareas de imagen](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Documentación del Asistente para publicación

El Asistente para publicación web y el Asistente para ordenación de impresión en línea se analizan en detalle en los documentos siguientes. También se han analizado las instrucciones para desarrollar aplicaciones que van a hospedarse en ellas.

-   [Diseño del lado cliente](pubwiz-client.md)
-   [Diseño del lado servidor](pubwiz-server.md)
-   [Registro de un servicio](pubwiz-reg.md)
-   [Uso del manifiesto de transferencia](pubwiz-manifest.md)
-   [Esquema de manifiesto de transferencia](/windows/desktop/shell/interfaces)

 

 