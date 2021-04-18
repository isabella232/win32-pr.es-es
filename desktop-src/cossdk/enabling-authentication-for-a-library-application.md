---
description: Habilitar la autenticación para una aplicación de biblioteca
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Habilitar la autenticación para una aplicación de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686448"
---
# <a name="enabling-authentication-for-a-library-application"></a>Habilitar la autenticación para una aplicación de biblioteca

Dado que las aplicaciones de biblioteca COM+ están hospedadas en otros procesos, sus requisitos de seguridad pueden ser diferentes de los de las aplicaciones de servidor. Si el explorador va a hospedar la aplicación de biblioteca, es posible que tenga que recibir devoluciones de llamada no autenticadas.

Para satisfacer esta necesidad, puede deshabilitar la autenticación para que el proceso de hospedaje no realice comprobaciones de seguridad para los llamadores de la aplicación de biblioteca. Al deshabilitar la autenticación, las llamadas a la aplicación de biblioteca se desconectan de forma eficaz; todas las llamadas a ella se realizarán correctamente. Para obtener más información, vea [seguridad de aplicaciones de biblioteca](library-application-security.md).

**Para habilitar (o deshabilitar) la autenticación para una aplicación de biblioteca**

1.  Haga clic con el botón secundario en la aplicación COM+ para la que va a habilitar o deshabilitar la autenticación y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .

3.  En **autenticación**, active la casilla **Habilitar autenticación** para habilitar la autenticación; Si desactiva la casilla, se deshabilitará la autenticación.

4.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



