---
title: Sesiones de edición
description: Cuando un servicio de texto debe obtener, modificar o establecer texto en un contexto, debe solicitar una sesión de edición.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Marco de trabajo de servicios de texto (TSF), editar sesión
- TSF (marco de trabajo de servicios de texto), editar sesión
- servicios de texto, editar sesión
- sesión de edición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532434"
---
# <a name="edit-sessions"></a>Sesiones de edición

Cuando un servicio de texto debe obtener, modificar o establecer texto en un contexto, debe solicitar una *sesión de edición*. Cuando se solicita una sesión de edición, el administrador de TSF negocia con el propietario del contexto de destino un bloqueo de documento del tipo solicitado. Cuando se concede el bloqueo del documento, el administrador de TSF permite al servicio de texto leer o escribir texto en el contexto o desde él.

 

 




