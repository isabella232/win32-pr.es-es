---
description: Cuando establece un nivel de autenticación para una aplicación, determina el grado de autenticación que se realiza cuando los clientes realizan una llamada a la aplicación.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Establecer un nivel de autenticación para una aplicación de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6248574117a55420940fbaf24f88c5d3b2c8721e6fa022bad5923ba658bf5da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546259"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Establecer un nivel de autenticación para una aplicación de servidor

Cuando establece un nivel de autenticación para una aplicación, determina el grado de autenticación que se realiza cuando los clientes realizan una llamada a la aplicación. Los niveles de autenticación más altos proporcionan mayor seguridad e integridad de los datos, aunque normalmente con cierta degradación del rendimiento. Para obtener más información, vea [Autenticación de cliente.](client-authentication.md)

**Para seleccionar un nivel de autenticación para una aplicación de servidor**

1.  Haga clic con el botón derecho en la aplicación COM+ para la que va a establecer la autenticación y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo propiedades de la aplicación, haga clic en **la pestaña** Seguridad .

3.  En el **cuadro Authentication level for calls (Nivel de** autenticación para llamadas), seleccione el nivel adecuado. Los niveles son los siguientes, ordenados de menor a mayor seguridad:

    -   **No**. no se realiza ninguna autenticación.
    -   **Conectar**. Autentica las credenciales solo cuando la conexión está establecida.
    -   **Llame a**. Autentica las credenciales al principio de cada llamada.
    -   **Paquete**. Realiza autenticación de las credenciales y comprueba si todos los datos de la llamada se han recibido. Ésta es la configuración predeterminada para las aplicaciones de servidor COM+.
    -   **Integridad de paquetes**. Realiza la autenticación de las credenciales y comprueba si algún dato de la llamada se ha modificado durante la transmisión.
    -   **Privacidad de paquetes**. Realiza autenticación de credenciales y cifra el paquete, incluidos los datos y la identidad y firma del remitente.

4.  Haga clic en **Aceptar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



