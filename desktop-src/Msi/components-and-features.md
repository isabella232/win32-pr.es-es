---
description: El Windows organiza una instalación en torno a los conceptos de componentes y características.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Componentes y características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cea0d384b3ad2bc3238178ae0f5811c3bad7b501068bcecd35d4c5b36d922a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144561"
---
# <a name="components-and-features"></a>Componentes y características

El Windows organiza una instalación en torno a los conceptos de componentes y características.

Una característica forma parte de la funcionalidad total de la aplicación que un usuario puede decidir instalar de forma independiente. Para obtener más información, [vea Windows Installer Features](windows-installer-features.md).

Un componente es una parte de la aplicación o el producto que se va a instalar. El instalador siempre instala o quita un componente del equipo de un usuario como una pieza coherente. Normalmente, los componentes se ocultan al usuario. Cuando un usuario selecciona una característica para la instalación, el instalador determina qué componentes deben instalarse para proporcionar esa característica. Para obtener más información, [vea Windows Installer Components](windows-installer-components.md).

Los autores de paquetes de instalación deben decidir cómo dividir su aplicación en características y componentes. La selección de características viene determinada principalmente por la funcionalidad de la aplicación desde la perspectiva del usuario. Dado que los componentes normalmente se deben compartir entre aplicaciones o incluso entre productos, se recomienda que los autores sigan un método estándar para seleccionar componentes. Para obtener más información, [vea Organización de aplicaciones en componentes](organizing-applications-into-components.md).

 

 



