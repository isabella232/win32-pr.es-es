---
description: Para usar la seguridad basada en roles en la aplicación COM+, primero debe habilitar la comprobación de la autorización basada en roles para la aplicación.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Habilitar la comprobación de la autorización de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080234"
---
# <a name="enabling-role-based-authorization-checking"></a>Habilitar la comprobación de la autorización de Role-Based

Para usar la seguridad basada en roles en la aplicación COM+, primero debe habilitar la comprobación de la autorización basada en roles para la aplicación. Esto garantiza que los usuarios que tienen acceso a la aplicación se comprueban para el rol al que pertenecen antes de que estén autorizados para realizar cualquier acción en la aplicación. Si la comprobación de la autorización basada en roles no está habilitada, no se utiliza la seguridad basada en roles de la aplicación.

**Para habilitar la comprobación de la autorización basada en roles**

1.  Haga clic con el botón secundario en la aplicación COM+ para la que va a habilitar la comprobación de la autorización basada en roles y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .

3.  En **autorización**, active la casilla **exigir comprobaciones de acceso para esta aplicación** ; la desactivación de la casilla significa que la seguridad basada en roles no se utiliza para la aplicación.

4.  Haga clic en **OK**.

La configuración de autorización seleccionada tendrá efecto la próxima vez que se inicie la aplicación.

 

 



