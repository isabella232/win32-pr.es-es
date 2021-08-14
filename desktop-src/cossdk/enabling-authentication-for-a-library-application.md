---
description: Habilitación de la autenticación para una aplicación de biblioteca
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Habilitación de la autenticación para una aplicación de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bceb3d5799ee8fac1d8eb266e6513c4d2a759adb10b78b2117424b08f8c5d6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736424"
---
# <a name="enabling-authentication-for-a-library-application"></a>Habilitación de la autenticación para una aplicación de biblioteca

Dado que las aplicaciones de biblioteca COM+ se hospedan en otros procesos, sus requisitos de seguridad pueden ser diferentes de los de las aplicaciones de servidor. Si un explorador hospedará la aplicación de biblioteca, es posible que tenga que recibir devoluciones de llamada no autenticadas.

Para solucionar esta necesidad, puede deshabilitar la autenticación para que el proceso de hospedaje no realice comprobaciones de seguridad para los autores de llamadas de la aplicación de biblioteca. Al deshabilitar la autenticación, las llamadas a la aplicación de biblioteca no se autentican de forma eficaz; todas las llamadas a ella se realizará correctamente. Para obtener más información, vea [Library Application Security](library-application-security.md).

**Para habilitar (o deshabilitar) la autenticación para una aplicación de biblioteca**

1.  Haga clic con el botón derecho en la aplicación COM+ para la que va a habilitar o deshabilitar la autenticación y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo propiedades de la aplicación, haga clic en **la pestaña** Seguridad.

3.  En **Autenticación**, active la **casilla Habilitar** autenticación para habilitar la autenticación; Al desactivar la casilla se deshabilitará la autenticación.

4.  Haga clic en **Aceptar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer un nivel de autenticación para una aplicación de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



