---
description: A partir Windows 7, los menús en cascada se crean a través de la entrada del Registro SubCommands, la entrada del Registro ExtendedSubCommandsKey o la interfaz IExplorerCommand.
title: Crear menús estáticos en cascada
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 22fdc261012697affd99b5a1491ef5829fcc5329d5570ae4e3c37dcd111b457f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456335"
---
# <a name="creating-static-cascading-menus"></a>Crear menús estáticos en cascada

En Windows 7 y versiones posteriores, la implementación del menú en cascada se admite a través de la configuración del Registro. Antes de Windows 7, la creación de menús en cascada solo era posible mediante la implementación de la [**interfaz IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) En Windows 7 y versiones posteriores, debe recurrir a las soluciones basadas en código del Modelo de objetos componentes (COM) solo cuando los métodos estáticos no son suficientes.

La siguiente captura de pantalla proporciona un ejemplo de un menú en cascada.

![captura de pantalla que muestra un ejemplo de un menú en cascada](images/file-assoc/filecascademenu2ndex.png)

En Windows 7 y versiones posteriores, hay tres maneras de crear menús en cascada, que se describen en las secciones siguientes.

-   [Cómo crear menús en cascada con la entrada del Registro SubCommands](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Cómo crear menús en cascada con la entrada del Registro ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Cómo crear menús en cascada con la interfaz IExplorerCommand](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
