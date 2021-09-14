---
description: Ejemplo de intercambio de paquetes del Protocolo SMB de Microsoft entre un cliente y un servidor.
ms.assetid: f831d0de-0e38-4141-811c-892a1b5c4037
title: Escenario de paquetes de protocolo SMB Exchange Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a03e2f75b00aa93e629b3e698631c5efde4694
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069908"
---
# <a name="microsoft-smb-protocol-packet-exchange-scenario"></a>Escenario de paquetes de protocolo SMB Exchange Microsoft

En este tema se proporciona un ejemplo de intercambio de paquetes del Protocolo SMB de Microsoft entre un cliente y un servidor. Los pasos siguientes son una introducción al proceso:

1.  El cliente y el servidor establecen una sesión NetBIOS.
2.  El cliente y el servidor negocian el dialecto del protocolo SMB de Microsoft.
3.  El cliente inicia sesión en el servidor.
4.  El cliente se conecta a un recurso compartido en el servidor.
5.  El cliente abre un archivo en el recurso compartido.
6.  El cliente lee del archivo.

En primer lugar, el cliente establece una conexión TCP de dúplex completo con el servidor. A continuación, el cliente compila y envía un paquete de solicitud de sesión NetBIOS a través de la conexión TCP. Si el formato del paquete se ha dado correctamente, el servidor devuelve un paquete que contiene un mensaje que confirma que se ha establecido la sesión. Después de esto, el cliente envía los primeros paquetes del Protocolo SMB de Microsoft al servidor.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Paquete 1: SMB \_ COM \_ NEGOTIATE**<br/> **Dirección:** Cliente a servidor<br/> **Descripción:** El cliente solicita que el servidor negocie el dialecto del protocolo SMB de Microsoft. En el paquete se incluye una lista de cadenas que identifican los dialectos con los que el cliente puede trabajar.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Paquete 2: SMB \_ COM \_ NEGOTIATE**<br/> **Dirección:** Servidor a cliente<br/> **Descripción:** El servidor responde a la solicitud del cliente para identificar el dialecto del protocolo SMB de Microsoft que se va a usar en la sesión. El paquete devuelto también incluye una cadena aleatoria de 8 bytes que se usará en el paso siguiente para autenticar al cliente durante el proceso de inicio de sesión.<br/>                                                                                                                                                                                                                                   |
| **Paquete 3: CONFIGURACIÓN \_ DE SESIÓN COM SMB \_ \_ \_ ANDX**<br/> **Dirección:** Cliente a servidor<br/> **Descripción:** Este paquete incluye información sobre las funcionalidades de cliente, por lo que este paquete debe enviarse incluso si el servidor solo ha implementado la seguridad de nivel de recurso compartido.<br/> **Paquete 3: CONFIGURACIÓN \_ DE SESIÓN COM SMB \_ \_ \_ ANDX**<br/> **Dirección:** Servidor a cliente<br/> **Descripción:** Si el servidor acepta el desafío o la respuesta, se incluye un UID válido en el paquete que se devuelve al cliente. Si no se acepta, el servidor devolverá un código de error en este paquete y denegará el acceso.<br/> |
| **Paquete 4: SMB \_ COM \_ TREE CONNECT \_ \_ ANDX**<br/> **Dirección:** Cliente a servidor<br/> **Descripción:** El cliente solicita acceso al recurso compartido. El paquete contiene la ruta de acceso completa del recurso compartido en formato UNC.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| **Paquete 5: SMB \_ COM \_ TREE CONNECT \_ \_ ANDX**<br/> **Dirección:** Servidor a cliente<br/> **Descripción:** Si se concede acceso al recurso compartido, el servidor devuelve el identificador de árbol de 16 bits (TID) que corresponde al recurso compartido de este paquete. Si el recurso compartido no existe o el usuario no tiene credenciales suficientes para acceder al recurso compartido, el servidor devolverá un código de error en este paquete y denegará el acceso al recurso compartido.<br/>                                                                                                                                                                                                 |
| **Paquete 6: SMB \_ COM \_ OPEN \_ ANDX**<br/> **Dirección:** Cliente a servidor<br/> **Descripción:** El cliente solicita al servidor que abra un archivo en el recurso compartido al que se accede en nombre del cliente. Este paquete contiene el nombre del archivo que se va a abrir.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| **Paquete 7: SMB \_ COM \_ OPEN \_ ANDX**<br/> **Dirección:** Servidor a cliente<br/> **Descripción:** Si se concede acceso al archivo, el servidor devuelve el identificador de archivo del archivo solicitado. Si el archivo no existe o el usuario no tiene credenciales suficientes para acceder al archivo, el servidor devolverá un código de error en este paquete y denegará el acceso al archivo.<br/>                                                                                                                                                                                                                                                  |
| **Paquete 8: SMB \_ COM \_ READ \_ ANDX**<br/> **Dirección:** Cliente a servidor<br/> **Descripción:** El cliente solicita al servidor que lea los datos del archivo abierto en nombre del cliente y devuelva estos datos al cliente. El identificador de archivo que obtiene el cliente cuando se abrió el archivo se incluye en este paquete con el fin de identificar de qué archivo abierto debe leer los datos el servidor.<br/>                                                                                                                                                                                                                   |
| **Paquete 9: SMB \_ COM \_ READ \_ ANDX**<br/> **Dirección:** Servidor a cliente<br/> **Descripción:** El servidor devuelve los datos de archivo solicitados en este paquete. Es poco probable que se produzca un error, dado que se ha concedido acceso al servidor, al recurso compartido y al archivo. Sin embargo, puede ocurrir en algunas situaciones: por ejemplo, si se cambia el acceso a un recurso compartido entre el momento en que se abre el archivo y el momento en que se lee.<br/>                                                                                                                                                                                                      |



 

> [!Note]  
> Si implementa un CIFS que no admite notificaciones de cambios, Windows puede mantener un identificador pendiente en el sistema de archivos y la conexión SMB puede desaparecer sin previo aviso.

 

 

 




