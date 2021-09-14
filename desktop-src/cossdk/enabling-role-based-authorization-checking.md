---
description: Para usar la seguridad basada en roles en la aplicación COM+, primero debe habilitar la comprobación de autorización basada en roles para la aplicación.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Habilitación de Role-Based comprobación de autorización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160502"
---
# <a name="enabling-role-based-authorization-checking"></a>Habilitación de Role-Based comprobación de autorización

Para usar la seguridad basada en roles en la aplicación COM+, primero debe habilitar la comprobación de autorización basada en roles para la aplicación. Esto garantiza que los usuarios que acceden a la aplicación se comprueban el rol al que pertenecen antes de que estén autorizados a hacer nada en la aplicación. Si la comprobación de autorización basada en roles no está habilitada, no se usa la seguridad basada en roles para la aplicación.

**Para habilitar la comprobación de autorización basada en roles**

1.  Haga clic con el botón derecho en la aplicación COM+ para la que va a habilitar la comprobación de autorización basada en roles y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo propiedades de la aplicación, haga clic en **la pestaña** Seguridad.

3.  En **Autorización**, active la casilla **Aplicar comprobaciones de** acceso para esta aplicación; Desactivar la casilla significa que la seguridad basada en roles no se usa para la aplicación.

4.  Haga clic en **OK**.

La configuración de autorización seleccionada tiene efecto la próxima vez que se inicia la aplicación.

 

 



