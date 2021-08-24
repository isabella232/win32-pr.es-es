---
title: Migración del controlador de gráficos a Windows 10
description: Windows 10 Los medios Windows 10, al igual que su predecesor, Windows 8.1, no tienen controladores de gráficos de terceros en el kit de medios de Windows ni en "In Box".
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b1703210318f55dad3e50f4dcdd7e143434275b7ef3b41203f41792262a53e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882715"
---
# <a name="graphics-driver-migration-to-windows-10"></a>Migración del controlador de gráficos a Windows 10

Windows 10 Los medios Windows 10, al igual que su predecesor, Windows 8.1, no tienen controladores de gráficos de terceros en el kit de medios de Windows ni en "In Box". En su lugar, los controladores de gráficos para una amplia gama de dispositivos se aprovisionan en WU, lo que permite a los proveedores de hardware actualizar los controladores sin necesidad de un cambio en la imagen del sistema operativo. Además, los controladores existentes no se migran a Windows 10 durante una actualización del sistema operativo a Windows 10 desde Windows 7, Windows 8 o Windows 8.1. Esto también afecta a las actualizaciones de Windows Server 2012.

## <a name="upgrades-and-installation"></a>Actualizaciones e instalación

Para las actualizaciones y las nuevas instalaciones, los controladores de gráficos deben obtenerse de Windows Update (WU) o del sitio web de IHV/OEM para el hardware correspondiente. Para hacerlo, se necesita una conexión a Internet. Los controladores de WU se insertan en la configuración del sistema operativo mediante la actualización dinámica (DU) cuando un usuario actualiza su sistema Windows 7 o Windows 8.x para Windows 10.

> [!Note]  
> Esto no se aplica a los sistemas que Windows instalados previamente, por ejemplo, equipos fuera de servicio adquiridos en una tienda minorista. Estos sistemas ya tienen los controladores de gráficos instalados por el OEM. El OEM también podría proporcionar un DVD (para volver a instalar el sistema operativo) que incluye los controladores.

 

Después de actualizar a Windows 10, es posible que los usuarios encuentren que no hay controladores de gráficos instalados en su equipo. Esto puede ocurrir por diversas razones:

-   El usuario eligió realizar una instalación limpia, es decir, no una actualización.
-   El usuario desactivó la opción para buscar actualizaciones durante la actualización, es decir, la actualización dinámica (DU) deshabilitada de forma eficaz.
-   La conexión a Internet no funcionaba durante la actualización.
-   Error en la instalación del controlador.

Después de una instalación limpia del sistema operativo, no habrá ningún controlador de gráficos en el equipo hasta que el cliente de WU se ejecute automáticamente y descargue los controladores aplicables. Entre tanto, el equipo estará ejecutando el adaptador de pantalla básico de Microsoft (MSBDA), que tiene funcionalidades limitadas, por ejemplo, sin compatibilidad con varios monitores y el usuario también podría experimentar un rendimiento deficiente en comparación con un controlador de hardware, por ejemplo, velocidad de fotogramas lenta o desgarro en la reproducción de vídeo.

## <a name="manifestations"></a>Manifestaciones

En el caso de los equipos antiguos (normalmente creados antes de Windows 7), es posible que no haya controladores para Windows 10 en WU porque los adaptadores de gráficos han alcanzado el final del ciclo de vida (EOL) y los proveedores de hardware ya no son compatibles. Incluso los sistemas que Windows 7 u 8.x se podrían haber actualizado desde un sistema operativo anterior y podrían tener adaptadores de gráficos EOL.

Es posible que los equipos más recientes no tengan controladores disponibles porque el adaptador de gráficos se transfirieron desde un equipo anterior, por ejemplo, durante una actualización de hardware. Esto suele ocurrir en equipos con varios adaptadores de gráficos en los que el usuario conservaba una tarjeta gráfica antigua al comprar una nueva máquina con el fin de usar varias pantallas.

Otra posibilidad para un pequeño porcentaje de máquinas es que Windows Update solo tiene controladores de "cobertura". Se trata de controladores genéricos que carecen de personalizaciones de OEM. Un usuario que haya entregado uno de estos controladores después de actualizar a Windows 10 podría ver que falta alguna funcionalidad, por ejemplo, las teclas de función para controlar el brillo de la pantalla ya no funcionan.

## <a name="mitigations"></a>Mitigaciones

-   Los controladores de gráficos adecuados deben entregarse mediante DU durante el proceso de actualización o por WU poco después de que se complete la actualización. Los OEM deben asegurarse de que los controladores de gráficos adecuados se incluyen en las imágenes del sistema que se usan para la instalación de fábrica Windows 10 en sus equipos.
-   Después de una actualización, el usuario puede comprobar explícitamente Configuración Windows update para los controladores, aunque \\ esto no debería ser necesario. Los usuarios que fuerzan una comprobación mientras se instala automáticamente un controlador en segundo plano podrían ver un error de instalación del controlador si la instalación automática se completa primero. Esto se puede omitir.
-   Los usuarios que pretenden realizar una instalación limpia de Windows 10 deben obtener los controladores pertinentes antes de instalar o confiar en Windows Update para proporcionar los controladores más adelante, en cuyo caso deben asegurarse de que su conexión a Internet funciona.
-   En el caso de los equipos que reciben un controlador de cobertura, no hay ninguna mitigación para la funcionalidad que falta. Sin embargo, esto solo debería ocurrir en los casos en los que el proveedor de hardware ya no mantiene los controladores, es decir, equipos con varios años de antigüedad.

> [!Note]  
> En el caso de los sistemas con una sola pantalla, por ejemplo, un portátil, muchos usuarios descubren que MSBDA es aceptable y no observan la falta de un controlador de hardware. En este caso, no se requiere ninguna mitigación.

 

## <a name="solutions"></a>Soluciones

Es fundamental que los OEM y los IHV carguen sus controladores de gráficos Windows 10 en WU para cualquier hardware que pretendan admitir.

Los usuarios deben dejar seleccionada la opción "Buscar actualizaciones" (la configuración predeterminada) al actualizar. Dependiendo de la velocidad de la conexión de red y de la carga en los servidores WU, esto puede significar que los controladores no se instalan hasta que se haya completado OOBE y el usuario haya iniciado sesión por primera vez. Mientras tanto, el usuario podría observar alguna funcionalidad limitada o un rendimiento deficiente.

Los usuarios deben asegurarse de que su conexión a Internet funciona antes de iniciar una actualización, incluso si están actualizando mediante medios (DVD o unidad flash).

-   Si el equipo está conectado a Internet, se deben descargar e instalar automáticamente los controladores adecuados. El usuario no tiene que realizar ninguna acción.
-   Si el equipo no está conectado a Internet, los controladores se deben descargar desde el sitio web de IHV o OEM mediante un equipo conectado a Internet. se transfieren a la máquina de destino mediante una unidad flash o CD/DVD; y, a continuación, se instalan manualmente.

 

 




