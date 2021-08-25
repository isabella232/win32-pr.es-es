---
title: Implementación Active Accessibility nativa
description: Se dice que los elementos de la interfaz de usuario que implementan la interfaz IAccessible proporcionan una implementación nativa.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4414fa1cd40b66b0971d7c74f484b90c62f86db64722abaabc0e8eea60b14fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859935"
---
# <a name="native-active-accessibility-implementation"></a>Implementación Active Accessibility nativa

Se dice que los elementos de la interfaz de usuario que implementan [**la interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan una *implementación nativa.* Aunque el costo de desarrollo para implementar **IAccessible** (o cualquier otra interfaz del modelo de objetos componentes (COM) puede ser alto, la ventaja es un control completo sobre la información expuesta a los clientes.

Si la aplicación usa controles personalizados u otros controles que no se pueden Oleacc.dll mediante proxy, deberá proporcionar una implementación nativa.

 

 




