---
description: Una acción personalizada en una tabla de secuencia de interfaz de usuario o un archivo ejecutable externo puede necesitar el nivel de interfaz de usuario actual de la instalación.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Determinar el nivel de la interfaz de usuario a partir de una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158590"
---
# <a name="determining-ui-level-from-a-custom-action"></a>Determinar el nivel de la interfaz de usuario a partir de una acción personalizada

Una acción personalizada en una tabla de secuencia de interfaz de usuario o un archivo ejecutable externo puede necesitar el nivel de interfaz de usuario actual de la instalación. Por ejemplo, una acción personalizada que tiene un cuadro de diálogo solo debe mostrar el cuadro de diálogo cuando el nivel de interfaz de usuario es Interfaz de usuario completa o Interfaz de usuario reducida, no debe mostrar el cuadro de diálogo si el nivel de interfaz de usuario es Interfaz de usuario básica o Ninguno. Debe usar la propiedad [**UILevel**](uilevel.md) para determinar el nivel de interfaz de usuario actual. No se puede llamar a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) desde una acción personalizada y no es posible cambiar la propiedad de nivel de interfaz de usuario desde dentro de una acción personalizada.

Se recomienda que las acciones personalizadas no usen el nivel de interfaz de usuario como condición para enviar mensajes de error al instalador, ya que esto puede interferir con el registro y los mensajes externos.

 

 



