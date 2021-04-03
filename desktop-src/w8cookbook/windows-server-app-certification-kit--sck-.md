---
title: Herramienta de prueba de Microsoft Platform Ready
description: Herramienta de prueba de Microsoft Platform Ready
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794194"
---
# <a name="microsoft-platform-ready-test-tool"></a>Herramienta de prueba de Microsoft Platform Ready

## <a name="platform"></a>Plataforma

 **Servidores** : windows Server 2012 \| Windows Server 2012 R2  

## <a name="description"></a>Descripción

La herramienta de prueba preparación para la plataforma de Microsoft (MPR) se usa para preparar las aplicaciones de la plataforma y para validar el cumplimiento de los requisitos de certificación de las aplicaciones Windows Server 2012 y Windows Server 2012 R2.

Microsoft recomienda encarecidamente incorporar la herramienta de prueba de MPR en los procesos de compilación y prueba de software, lo que garantiza la disponibilidad de la plataforma antes de que las aplicaciones se publiquen en el mercado. La herramienta de prueba de MPR también es una herramienta recomendada para probar las aplicaciones de línea de negocio y para evaluar los productos de servidor para su compatibilidad con la plataforma antes de tomar decisiones de compra.

## <a name="requirements"></a>Requisitos

La herramienta de prueba de MPR incluye pruebas automatizadas para:

-   Windows Installer
-   Instalación y funcionalidad principal
-   Controladores y seguridad
-   Prácticas recomendadas

La prueba automática y el envío de los resultados de la mayoría de las aplicaciones de servidor deben tardar 2 horas o menos. las aplicaciones más complejas pueden tardar aproximadamente 4 horas.

Todos los controladores deben pasar por separado las pruebas de certificación de hardware de Windows y estar firmadas por Microsoft para Windows Server 2012.

## <a name="usage"></a>Uso

Para probar sus aplicaciones:

1.  Instale la configuración mínima más reciente de Windows Server 2012 (GUI de servidor completa, interfaz de servidor mínima o Server Core) según sea necesario para la aplicación.
2.  Revise los requisitos de certificación.
3.  En un sistema limpio, ejecute la herramienta de prueba de MPR en modo de interfaz de usuario completa o en modo de línea de comandos.
4.  Complete el proceso de prueba autoguiado.
5.  Revise los resultados y corrija la aplicación según sea necesario.
6.  Iniciar sesión y cargar los resultados correctos en el portal de la plataforma de Microsoft listo para la publicación en el catálogo de Windows Server y el uso del logotipo.

## <a name="resources"></a>Recursos

-   [Requisitos para el programa de certificación de aplicaciones de Windows Server](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Herramienta de comprobación Microsoft Platform Ready (MPR)](https://www.microsoft.com/download/details.aspx?id=37143)
-   [Programa de certificación de aplicaciones de Windows Server 2012](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [Comentarios del logotipo de Windows Server](mailto:WSLogoFB@microsoft.com)

 

 