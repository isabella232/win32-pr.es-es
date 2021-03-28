---
description: 'Otra opción para agregar verbos a un menú en cascada es a través de IExplorerCommand:: EnumSubCommands.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Crear menús en cascada con la interfaz IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104563422"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Cómo crear menús en cascada con la interfaz IExplorerCommand

Otra opción para agregar verbos a un menú en cascada es a través de [**IExplorerCommand:: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Este método habilita los orígenes de datos que proporcionan los comandos del módulo de comandos a través de la interfaz [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) para usar esos comandos como verbos en un menú contextual. En Windows 7 y versiones posteriores, puede proporcionar la misma implementación de verbo mediante la interfaz [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) que puede con la interfaz [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .

## <a name="instructions"></a>Instrucciones


En las dos capturas de pantalla siguientes se muestra el uso de menús en cascada en la carpeta **dispositivos** .

![Captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos.](images/file-assoc/filecascademenu.png)

![captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta dispositivos](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a>Observaciones

> [!Note]  
> Dado que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) solo admite la activación en proceso, se recomienda para su uso por parte de los orígenes de datos de Shell que necesitan compartir la implementación entre los comandos y los menús contextuales.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
