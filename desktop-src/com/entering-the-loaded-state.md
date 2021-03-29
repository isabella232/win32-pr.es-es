---
title: Entrando en el estado cargado
description: Entrando en el estado cargado
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774977"
---
# <a name="entering-the-loaded-state"></a>Entrando en el estado cargado

Cuando un objeto entra en el estado de carga, se crean las estructuras en memoria que representan el objeto para que se puedan invocar las operaciones en él. Se carga el controlador del objeto o el servidor en proceso. Este proceso, al que se hace referencia como *creación de instancias*, se produce cuando se carga un objeto desde el almacenamiento persistente (una transición del estado pasivo al estado cargado) o cuando se crea un objeto por primera vez.

Internamente, la creación de instancias es un proceso de dos fases. Se crea un objeto de la clase adecuada, después del cual se llama a un método en ese objeto para realizar la inicialización y dar acceso a los datos del objeto. El método de inicialización se define en una de las interfaces admitidas del objeto. El método de inicialización determinado llamado depende del contexto en el que se crea una instancia del objeto y de la ubicación de los datos de inicialización.

 

 




