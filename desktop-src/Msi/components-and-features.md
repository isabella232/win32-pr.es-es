---
description: El Windows Installer organiza una instalación en torno a los conceptos de componentes y características.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Componentes y características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155140"
---
# <a name="components-and-features"></a>Componentes y características

El Windows Installer organiza una instalación en torno a los conceptos de componentes y características.

Una característica forma parte de la funcionalidad total de la aplicación que un usuario puede decidir instalar de forma independiente. Para obtener más información, vea [características de Windows Installer](windows-installer-features.md).

Un componente es una parte de la aplicación o del producto que se va a instalar. El instalador siempre instala o quita un componente del equipo de un usuario como una pieza coherente. Los componentes suelen estar ocultos para el usuario. Cuando un usuario selecciona una característica para la instalación, el instalador determina qué componentes deben instalarse para proporcionar esa característica. Para obtener más información, vea [componentes de Windows Installer](windows-installer-components.md).

Los autores de los paquetes de instalación deben decidir cómo dividir la aplicación en características y componentes. La selección de características viene determinada principalmente por la funcionalidad de la aplicación desde la perspectiva del usuario. Dado que los componentes normalmente se deben compartir entre las aplicaciones, o incluso entre productos, se recomienda que los autores sigan un método estándar para seleccionar los componentes. Para obtener más información, vea [organizar aplicaciones en componentes](organizing-applications-into-components.md).

 

 



