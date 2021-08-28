---
description: La resistencia es la capacidad de una aplicación para recuperarse correctamente de situaciones en las que falta un componente vital o se ha reemplazado por una versión incompatible.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73565a129c25b19e0fb362e5363626f1acfee0387b2d4e4826f79222e7425b96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810785"
---
# <a name="resiliency"></a>Resistencia

La resistencia es la capacidad de una aplicación para recuperarse correctamente de situaciones en las que falta un componente vital o se ha reemplazado por una versión incompatible. Al crear un paquete de instalación y usar las funciones del instalador [,](installer-functions.md)los desarrolladores pueden usar el instalador de Windows para generar aplicaciones resistentes capaces de recuperarse de tales situaciones.

-   Use la lista de origen del instalador para aumentar la resistencia de las aplicaciones que dependen de los recursos de red. Para obtener más información, vea [Resistencia de origen.](source-resiliency.md)
-   Use la API del instalador para comprobar si está instalada una característica, un componente, un archivo o una versión de archivo vitales.
-   Use la API del instalador para comprobar la ruta de acceso a un componente en tiempo de ejecución. Esto reduce la dependencia de la aplicación en las rutas de acceso a archivos estáticos, que normalmente difieren entre equipos.
-   Use el instalador para volver a instalar los accesos directos dañados, las entradas del Registro y otros componentes sin tener que volver a ejecutar el programa de instalación.
-   Aumente la resistencia de la instalación del producto al dejar habilitada la funcionalidad de reversión del instalador. Para obtener más información, vea [Rollback Installation](rollback-installation.md).

 

 



