---
description: La resistencia es la capacidad de una aplicación para recuperarse correctamente de las situaciones en las que falta un componente vital o se ha reemplazado por una versión incompatible.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668358"
---
# <a name="resiliency"></a>Resistencia

La resistencia es la capacidad de una aplicación para recuperarse correctamente de las situaciones en las que falta un componente vital o se ha reemplazado por una versión incompatible. Mediante la creación de un paquete de instalación y el uso de las [funciones del instalador](installer-functions.md), los desarrolladores pueden utilizar la Windows Installer para generar aplicaciones resistentes capaces de recuperarse de estas situaciones.

-   Use la lista de origen del instalador para aumentar la resistencia de las aplicaciones que se basan en los recursos de red. Para obtener más información, consulte [resistencia del origen](source-resiliency.md).
-   Use la API del instalador para comprobar si hay instalada una versión vital de la característica, el componente, el archivo o el archivo.
-   Use la API del instalador para comprobar la ruta de acceso a un componente en tiempo de ejecución. Esto reduce la dependencia de la aplicación en rutas de acceso de archivo estáticas, que suelen diferir entre equipos.
-   Use el instalador para volver a instalar los accesos directos, las entradas del registro y otros componentes dañados sin tener que volver a ejecutar el programa de instalación.
-   Aumente la resistencia de la instalación del producto manteniendo habilitada la funcionalidad de reversión del instalador. Para obtener más información, consulte [reversión de instalación](rollback-installation.md).

 

 



