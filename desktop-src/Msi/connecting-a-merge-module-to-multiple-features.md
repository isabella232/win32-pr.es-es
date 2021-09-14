---
description: El Conectar del objeto merge se puede usar para conectar un módulo a una característica adicional que se ha combinado en la base de datos o que se combinará en la base de datos. La característica debe existir antes de llamar a este método.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Conectar un módulo de combinación a varias características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158781"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Conectar un módulo de combinación a varias características

El [**Conectar**](merge-connect.md) del objeto [](merge-object.md) merge se puede usar para conectar un módulo a una característica adicional que se ha combinado en la base de datos o que se combinará en la base de datos. La característica debe existir antes de llamar a este método.

Un módulo de combinación nunca debe entregar un componente que contenga archivos del sistema a la característica principal de una aplicación, ya que esto puede hacer que el instalador valide y repare la aplicación cada vez que se usa el archivo del sistema. Se .msi crear un archivo de .msi diseñado para aceptar componentes de un módulo de combinación para que los componentes que contienen archivos del sistema solo pertenezcan a características independientes de la característica principal de la aplicación.

Si el paquete usa un módulo de combinación que contiene archivos del sistema que vinculan todos los componentes del módulo de combinación a la característica principal de la aplicación, un intento de usar el archivo del sistema puede desencadenar el instalador para intentar reparar la característica principal de la aplicación. Si no se puede reparar la característica principal, se puede producir un error en la instalación.

 

 



