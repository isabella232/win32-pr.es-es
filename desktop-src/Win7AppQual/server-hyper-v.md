---
description: Hyper-V de servidor
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Hyper-V de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3149f1c5faa98c9c61be884a193b0e3a1ecceb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569748"
---
# <a name="server-hyper-v"></a>Hyper-V de servidor

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows XP \| Windows Vista \| Windows 7  
**Servidores:** Windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

La virtualización de servidores permite que varios sistemas operativos se ejecuten en una sola máquina física como máquinas virtuales , lo que permite consolidar las cargas de trabajo de las máquinas de servidor infrautilizadas en un número menor de máquinas totalmente utilizadas. Windows 7 incluye varias mejoras en la versión Windows Server 2008:

-   **Migración en vivo:** En Windows Server 2008, teníamos migración rápida. Con Migración en vivo, hemos mejorado la velocidad de migración y la flexibilidad de almacenamiento.
-   **Compatibilidad con procesadores lógicos:** Hemos aumentado los procesadores de host lógico de 16LP a 64LP.
-   **Storage agregar en caliente:** Ahora puede agregar discos VHD o de paso a través adicionales a una máquina virtual en ejecución sin desactivar la máquina virtual.
-   **Nueva compatibilidad con hardware:** Hemos agregado compatibilidad con las tecnologías incluidas en los nuevos procesadores y tarjetas de red que se comercializan, incluida la traducción de segundo nivel (SLAT), la descarga TCP (Chimney) y VMdQ.
-   **Virtualización de Terminal Services (TSv):** Hemos centralizado la solución de escritorio para Hyper-V.

## <a name="manifestation-of-impact"></a>Demostración del impacto

-   **Migración en vivo:** Es posible que tenga que cambiar la forma en que ha diseñado los sistemas de almacenamiento para aprovechar completamente esta tecnología. Aunque es posible que estos cambios no sean necesarios, puede optar por implementarlos para aprovechar al máximo las ventajas. Es posible que necesite una aplicación de administración para organizar Migración en vivo.
-   **Compatibilidad con procesadores lógicos:** Esta característica no afectará a los clientes ni a los ISV al migrar de Windows Server 2008 a Windows Server 2008 R2.
-   **Storage agregar en caliente:** Esta característica no afectará a los clientes ni a los ISV al migrar de Windows Server 2008 a Windows Server 2008 R2. Las aplicaciones de administración que configuran las opciones de una máquina virtual pueden requerir actualización para administrar esta nueva característica.
-   **Nueva compatibilidad con hardware:** Estas características solo se aplican al nuevo hardware que se introduce en el mercado. Dado que no tendrá compatibilidad de compilación para estas características, es probable que un servidor físico que se migra de Windows Server 2008 a Windows Server 2008 R2 se verá afectado. Si estas características están disponibles en el servidor que se está migrando, no se prevé ningún cambio directo.
-   **Virtualización de Terminal Services:** Esta característica no afectará a los clientes ni a los ISV al migrar de Windows Server 2008 a Windows Server 2008 R2. Las aplicaciones que aprovechan Terminal Services (TS) pueden verse afectadas. Esta característica se integra directamente con TS y, por tanto, las aplicaciones que configuran TS pueden requerir actualización para administrar esta nueva característica.

## <a name="mitigation"></a>Mitigación

-   **Migración en vivo:** Proporcione instrucciones prescriptivas a los usuarios finales con procedimientos recomendados y recomendaciones para el diseño del sistema de almacenamiento. Debe informar al usuario final sobre las opciones y recomendaciones.

## <a name="leveraging-capabilitities"></a>Aprovechamiento de funcionalidades

-   **Migración en vivo:** Esta característica habilita el entorno de TI dinámico. Los desarrolladores de aplicaciones de Virtualization Management deben modificar su aplicación para aprovechar esta nueva característica. Microsoft hará que las interfaces WMI estén disponibles públicamente para permitir que un desarrollador integre aplicaciones con esta característica.
-   **Virtualización de Terminal Services:** Esta característica habilita un nuevo escenario de virtualización. Las aplicaciones que aprovechan Terminal Services (TS) pueden verse afectadas. Esta característica se integra directamente con TS y, por tanto, las aplicaciones que configuran TS pueden requerir actualización para administrar esta nueva característica.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

[Interfaces de administración wmi para Hyper-V v1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Aunque la mayor parte de este contenido se aplicará a la versión v2 de Hyper-V, una versión actualizada con información específica de v2 debe estar disponible más cerca del inicio Windows 7.

 

 
