---
description: Otra opción para agregar verbos a un menú en cascada es a través de IExplorerCommand::EnumSubCommands.
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Crear menús en cascada con la interfaz IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed12cf78dc4b5f6a77bbd00b06897b49474a401
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436100"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Cómo crear menús en cascada con la interfaz IExplorerCommand

Otra opción para agregar verbos a un menú en cascada es a través de [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Este método permite que los orígenes de datos que proporcionan sus comandos del módulo de comandos a través de la interfaz [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) usen esos comandos como verbos en un menú contextual. En Windows 7 y versiones posteriores, puede proporcionar la misma implementación de verbo mediante la interfaz [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) que con la [**interfaz IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)

## <a name="instructions"></a>Instrucciones


Las dos capturas de pantalla siguientes muestran el uso de menús en cascada en la **carpeta Dispositivos.**

![Captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta devices.](images/file-assoc/FileCascadeMenu.png)

![captura de pantalla que muestra un ejemplo de un menú en cascada en la carpeta devices](images/file-assoc/cascadeDevices2.png)

## <a name="remarks"></a>Observaciones

> [!Note]  
> Dado [**que IExplorerCommand solo**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) admite la activación en proceso, se recomienda su uso por parte de orígenes de datos de Shell que necesitan compartir la implementación entre comandos y menús contextuales.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
