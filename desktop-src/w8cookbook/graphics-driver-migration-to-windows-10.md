---
title: Migración del controlador de gráficos a Windows 10
description: Windows 10 media y Windows 10, como su predecesor, Windows 8.1, no tiene ningún controlador de gráficos de terceros en el kit de Windows Media o en Box.
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a23d8ae341172223955fcc781f95b7615bcfc867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704757"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migración del controlador de gráficos a Windows 10

Windows 10 media y Windows 10, como su predecesor, Windows 8.1, no tiene ningún controlador de gráficos de terceros en el kit de Windows Media o en Box. En su lugar, los controladores de gráficos de una amplia gama de dispositivos se aprovisionan en WU, lo que permite a los proveedores de hardware actualizar controladores sin necesidad de un cambio en la imagen de sistema operativo. Además, los controladores existentes no se migran a Windows 10 durante una actualización del sistema operativo a Windows 10 desde Windows 7, Windows 8 o Windows 8.1. Esto también afecta a las actualizaciones de Windows Server 2012.

## <a name="upgrades-and-installation"></a>Actualizaciones e instalación

En el caso de las actualizaciones y las nuevas instalaciones, los controladores de gráficos se deben obtener de Windows Update (WU) o del sitio web de IHV/OEM para el hardware pertinente. Para hacerlo, se necesita una conexión a Internet. La actualización dinámica (DU) inserta los controladores en WU cuando un usuario actualiza su sistema Windows 7 o Windows 8. x a Windows 10.

> [!Note]  
> Esto no se aplica a los sistemas que se instalan con Windows preinstalado, por ejemplo, equipos fuera del sistema adquiridos en una tienda. Estos sistemas ya tienen los controladores de gráficos instalados por el OEM. El OEM también puede proporcionar un DVD (para volver a instalar el sistema operativo) que incluye los controladores.

 

Después de actualizar a Windows 10, es posible que los usuarios descubran que no hay controladores de gráficos instalados en su equipo. Esto puede ocurrir por diversas razones:

-   El usuario eligió realizar una instalación limpia, es decir, no una actualización.
-   El usuario ha anulado la selección de la opción para comprobar si hay actualizaciones durante la actualización, es decir, se ha deshabilitado realmente la actualización dinámica (DU).
-   La conexión a Internet no funcionaba durante la actualización.
-   Error en la instalación del controlador.

Después de una instalación limpia del sistema operativo, no habrá controladores de gráficos en el equipo hasta que el cliente de WU se ejecute automáticamente y descargue los controladores aplicables. Mientras tanto, el equipo ejecutará el adaptador de pantalla básico de Microsoft (MSBDA), que tiene funcionalidades limitadas, por ejemplo, no se admiten varios monitores, y el usuario también puede experimentar un rendimiento deficiente en comparación con un controlador de hardware, por ejemplo, una velocidad de fotogramas lenta o un corte en la reproducción de vídeo.

## <a name="manifestations"></a>Manifestaciones

En el caso de equipos anteriores (que normalmente se compilaron antes de Windows 7), es posible que no haya Controladores para Windows 10 en WU porque los adaptadores de gráficos han llegado al final del ciclo de vida (EOL) y ya no son compatibles con los proveedores de hardware. Incluso los sistemas que actualmente ejecutan Windows 7 u 8. x se pueden haber actualizado desde un sistema operativo anterior y podrían haber caducados adaptadores de gráficos.

Es posible que los equipos más recientes no tengan controladores disponibles porque el adaptador de gráficos se transfirió desde un equipo anterior, por ejemplo, durante una actualización de hardware. Esto suele ocurrir en equipos con varios adaptadores de gráficos en los que el usuario mantiene una tarjeta gráfica antigua al adquirir una nueva máquina para usar varias pantallas.

Otra posibilidad para un pequeño porcentaje de máquinas es que Windows Update solo tiene controladores de "cobertura". Son controladores genéricos que carecen de personalizaciones de OEM. Un usuario que entregue uno de estos controladores después de actualizar a Windows 10 podría ver que falta alguna funcionalidad, por ejemplo, las teclas de función para controlar el brillo de la pantalla ya no funcionan.

## <a name="mitigations"></a>Mitigaciones

-   Los controladores de gráficos adecuados deben ser entregados por DU durante el proceso de actualización o por WU en cuanto se complete la actualización. Los OEM deben asegurarse de que los controladores de gráficos adecuados se incluyen en las imágenes de sistema usadas para la instalación de fábrica de Windows 10 en sus equipos.
-   Después de una actualización, el usuario puede comprobar explícitamente la configuración \\ Windows Update para los controladores, aunque no debería ser necesario. Los usuarios que fuerzan una comprobación mientras un controlador se instala automáticamente en segundo plano pueden ver un error de instalación del controlador si la instalación automática se completa primero. Esto se puede omitir.
-   Los usuarios que deseen realizar una instalación limpia de Windows 10 deben obtener los controladores relevantes antes de instalar o confiar en Windows Update para proporcionar los controladores más adelante, en cuyo caso deben asegurarse de que la conexión a Internet funciona.
-   En el caso de los equipos que reciben un controlador de cobertura, no hay ninguna mitigación para la funcionalidad que falta. Sin embargo, esto solo debería ocurrir en los casos en los que el proveedor de hardware ya no mantiene los controladores, es decir, los equipos que tienen varios años de antigüedad.

> [!Note]  
> En el caso de los sistemas con una sola pantalla, por ejemplo, un portátil, muchos usuarios encuentran que MSBDA es aceptable y no observan la falta de un controlador de hardware. En este caso no se requiere ninguna mitigación.

 

## <a name="solutions"></a>Soluciones

Es fundamental que los fabricantes de equipos originales (IHV) carguen sus controladores de gráficos de Windows 10 en WU para cualquier hardware que pretendan admitir.

Los usuarios deben dejar seleccionada la opción "buscar actualizaciones" (la configuración predeterminada) al actualizar. En función de la velocidad de la conexión de red y la carga en los servidores de WU, esto puede significar que los controladores no se instalen hasta que se haya completado OOBE y el usuario haya iniciado sesión por primera vez. Mientras tanto, el usuario podría observar una funcionalidad limitada o un rendimiento deficiente.

Los usuarios deben asegurarse de que la conexión a Internet funciona antes de iniciar una actualización, incluso si se están actualizando con medios (DVD o unidad flash).

-   Si el equipo está conectado a Internet, los controladores adecuados se deben descargar e instalar automáticamente. No es necesario que el usuario realice ninguna acción.
-   Si el equipo no está conectado a Internet, los controladores se deben descargar desde el sitio web de IHV o OEM mediante un equipo conectado a Internet. se transfiere a la máquina de destino mediante una unidad flash o un CD/DVD; y, a continuación, se instala manualmente.

 

 




