---
title: Sesiones de edición
description: Cuando un servicio de texto debe obtener, modificar o establecer texto en un contexto, debe solicitar una sesión de edición.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Text Services Framework (TSF),editar sesión
- TSF (Text Services Framework),editar sesión
- servicios de texto, editar sesión
- sesión de edición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243657"
---
# <a name="edit-sessions"></a>Sesiones de edición

Cuando un servicio de texto debe obtener, modificar o establecer texto en un contexto, debe solicitar una sesión *de edición*. Cuando se solicita una sesión de edición, el administrador de TSF negocia con el propietario del contexto de destino un bloqueo de documento del tipo solicitado. Cuando se concede el bloqueo de documento, el administrador de TSF permite al servicio de texto leer o escribir texto en el contexto o desde él.

 

 




