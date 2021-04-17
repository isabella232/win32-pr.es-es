---
description: Cuando establece un nivel de autenticación para una aplicación, determina el grado de autenticación que se realiza cuando los clientes realizan una llamada a la aplicación.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Establecer un nivel de autenticación para una aplicación de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705319"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Establecer un nivel de autenticación para una aplicación de servidor

Cuando establece un nivel de autenticación para una aplicación, determina el grado de autenticación que se realiza cuando los clientes realizan una llamada a la aplicación. Los niveles de autenticación más altos proporcionan mayor seguridad e integridad de los datos, aunque normalmente con cierta degradación del rendimiento. Para obtener más información, consulte [autenticación del cliente](client-authentication.md).

**Para seleccionar un nivel de autenticación para una aplicación de servidor**

1.  Haga clic con el botón secundario en la aplicación COM+ para la que está configurando la autenticación y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .

3.  En el cuadro **nivel de autenticación para llamadas** , seleccione el nivel adecuado. Los niveles son los siguientes, ordenados de menor a mayor seguridad:

    -   **No**. no se realiza ninguna autenticación.
    -   **Conéctese**. Autentica las credenciales solo cuando la conexión está establecida.
    -   **Llame a**. Autentica las credenciales al principio de cada llamada.
    -   **Paquete**. Realiza autenticación de las credenciales y comprueba si todos los datos de la llamada se han recibido. Ésta es la configuración predeterminada para las aplicaciones de servidor COM+.
    -   **Integridad del paquete**. Realiza la autenticación de las credenciales y comprueba si algún dato de la llamada se ha modificado durante la transmisión.
    -   **Privacidad de paquetes**. Realiza autenticación de credenciales y cifra el paquete, incluidos los datos y la identidad y firma del remitente.

4.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



