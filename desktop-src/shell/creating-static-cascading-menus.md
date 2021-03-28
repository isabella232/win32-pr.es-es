---
description: A partir de Windows 7, los menús en cascada se crean a través de la entrada del registro subcomandos, la entrada del registro ExtendedSubCommandsKey o la interfaz IExplorerCommand.
title: Crear menús en cascada estáticos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561443"
---
# <a name="creating-static-cascading-menus"></a>Crear menús en cascada estáticos

En Windows 7 y versiones posteriores, la implementación de menús en cascada se admite a través de la configuración del registro. Antes de Windows 7, la creación de menús en cascada solo era posible a través de la implementación de la interfaz [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . En Windows 7 y versiones posteriores, debe recurrir a las soluciones basadas en código del modelo de objetos componentes (COM) solo cuando los métodos estáticos no sean suficientes.

La siguiente captura de pantalla proporciona un ejemplo de un menú en cascada.

![captura de pantalla que muestra un ejemplo de un menú en cascada](images/file-assoc/filecascademenu2ndex.png)

En Windows 7 y versiones posteriores, hay tres maneras de crear menús en cascada, que se describen en las secciones siguientes.

-   [Cómo crear menús en cascada con la entrada del registro subcomandos](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Cómo crear menús en cascada con la entrada del registro ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Cómo crear menús en cascada con la interfaz IExplorerCommand](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
