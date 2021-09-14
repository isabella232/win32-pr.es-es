---
title: Implementación de Active Accessibility nativa
description: Se dice que los elementos de la interfaz de usuario que implementan la interfaz IAccessible proporcionan una implementación nativa.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070677"
---
# <a name="native-active-accessibility-implementation"></a>Implementación de Active Accessibility nativa

Se dice que los elementos de la interfaz de usuario que implementan [**la interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan una *implementación nativa.* Aunque el costo de desarrollo para implementar **IAccessible** (o cualquier otra interfaz del modelo de objetos componentes (COM) puede ser alto, la ventaja es un control completo sobre la información expuesta a los clientes.

Si la aplicación usa controles personalizados u otros controles que no se pueden Oleacc.dll mediante proxy, deberá proporcionar una implementación nativa.

 

 




