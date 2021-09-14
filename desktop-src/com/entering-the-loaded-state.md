---
title: Especificar el estado cargado
description: Especificar el estado cargado
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889132"
---
# <a name="entering-the-loaded-state"></a>Especificar el estado cargado

Cuando un objeto entra en el estado cargado, se crean las estructuras en memoria que representan el objeto para que se puedan invocar operaciones en él. Se carga el controlador del objeto o el servidor en proceso. Este proceso, denominado creación de *instancias,* se produce cuando se carga un objeto desde el almacenamiento persistente (una transición del estado pasivo al estado cargado) o cuando se crea un objeto por primera vez.

Internamente, la creación de instancias es un proceso de dos fases. Se crea un objeto de la clase adecuada, después del cual se llama a un método de ese objeto para realizar la inicialización y dar acceso a los datos del objeto. El método de inicialización se define en una de las interfaces admitidas del objeto. El método de inicialización concreto llamado depende del contexto en el que se crea una instancia del objeto y de la ubicación de los datos de inicialización.

 

 




