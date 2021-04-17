---
description: .
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Servidor Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6997074e000b17a119a838df5b6fab961b8ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717310"
---
# <a name="server-hyper-v"></a>Servidor Hyper-V

## <a name="platforms"></a>Plataformas

 **Clientes** -Windows XP Windows \| vista Windows \| 7  
**Servidores** : windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

La virtualización de servidores permite que varios sistemas operativos se ejecuten en una sola máquina física como máquinas virtuales (VM), lo que le permite consolidar cargas de trabajo de máquinas de servidor infrautilizados en un número menor de máquinas utilizadas por completo. Windows 7 incluye varias mejoras en la versión 2008 de Windows Server:

-   **Migración en vivo:** En Windows Server 2008, teníamos una migración rápida. Con Migración en vivo, se ha mejorado la velocidad de migración y la flexibilidad de almacenamiento.
-   **Compatibilidad con el procesador lógico:** Hemos aumentado el procesador de hosts lógicos de 16LP a 64LP.
-   **Adición de almacenamiento en caliente:** Ahora puede agregar más discos VHD o de acceso directo a una máquina virtual en ejecución sin apagar la máquina virtual.
-   **Nueva compatibilidad de hardware:** Hemos agregado compatibilidad con las tecnologías que se incluyen en los nuevos procesadores y las tarjetas de red que llegan al mercado, como la traducción de segundo nivel (SLAT), la descarga de TCP (Chimney) y VMdQ.
-   **Terminal Services virtualización (TSv):** Solución de escritorio centralizada para Hyper-V.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

-   **Migración en vivo:** Es posible que tenga que cambiar la manera en que ha diseñado los sistemas de almacenamiento con el fin de sacar el máximo partido de esta tecnología. Aunque es posible que estos cambios no sean necesarios, puede optar por implementarlos con el fin de aprovechar al máximo las ventajas. Es posible que necesite una aplicación de administración para orquestar Migración en vivo.
-   **Compatibilidad con el procesador lógico:** Esta característica no afectará a los clientes o fabricantes de software independientes al migrar de Windows Server 2008 a Windows Server 2008 R2.
-   **Adición de almacenamiento en caliente:** Esta característica no afectará a los clientes o fabricantes de software independientes al migrar de Windows Server 2008 a Windows Server 2008 R2. Es posible que sea necesario actualizar las aplicaciones de administración que configuran la configuración de una máquina virtual para poder administrar esta nueva característica.
-   **Nueva compatibilidad de hardware:** Estas características solo se aplican al nuevo hardware que se introduce en el mercado. Dado que no es compatible con la compilación de estas características, no es probable que se vea afectada un servidor físico que se está migrando desde Windows Server 2008 a Windows Server 2008 R2. Si estas características están disponibles en el servidor que se está migrando, no se prevé ningún cambio directo.
-   **Virtualización de Terminal Services:** Esta característica no afectará a los clientes o fabricantes de software independientes al migrar de Windows Server 2008 a Windows Server 2008 R2. Las aplicaciones que aprovechan Terminal Services (TS) pueden verse afectadas. Esta característica se integra directamente con TS y, por lo tanto, es posible que las aplicaciones que configuren TS deban actualizarse para poder administrar esta nueva característica.

## <a name="mitigation"></a>Mitigación

-   **Migración en vivo:** Proporcionar instrucciones prescriptivas a los usuarios finales con prácticas recomendadas y recomendaciones para el diseño del sistema de almacenamiento. Debe informar al usuario final acerca de las opciones y recomendaciones.

## <a name="leveraging-capabilitities"></a>Aprovechar Capabilitities

-   **Migración en vivo:** Esta característica habilita el entorno de ti dinámico. Los desarrolladores de aplicaciones de administración de virtualización deben modificar su aplicación para aprovechar esta nueva característica. Microsoft hará que las interfaces WMI estén disponibles públicamente para permitir que un desarrollador integre aplicaciones con esta característica.
-   **Virtualización de Terminal Services:** Esta característica permite un nuevo escenario de virtualización. Las aplicaciones que aprovechan Terminal Services (TS) pueden verse afectadas. Esta característica se integra directamente con TS y, por lo tanto, es posible que las aplicaciones que configuren TS deban actualizarse para poder administrar esta nueva característica.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

[Interfaces de administración de WMI para Hyper-V V1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Aunque la mayor parte de este contenido se aplicará a la versión 2 de Hyper-V, la versión actualizada debe estar disponible más cerca del lanzamiento de Windows 7.

 

 
