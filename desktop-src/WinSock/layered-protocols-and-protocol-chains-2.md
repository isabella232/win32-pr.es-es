---
description: 'Windows Sockets 2 incorpora el concepto de protocolo en capas: uno que implementa solo funciones de comunicaciones de nivel superior mientras se basa en una pila de transporte subyacente para el intercambio de datos real con un punto de conexión remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolos en capas y cadenas de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154269"
---
# <a name="layered-protocols-and-protocol-chains"></a>Protocolos en capas y cadenas de protocolo

Windows Sockets 2 incorpora el concepto de protocolo en capas: uno que implementa solo funciones de comunicaciones de nivel superior mientras se basa en una pila de transporte subyacente para el intercambio de datos real con un punto de conexión remoto. Un ejemplo de este tipo de protocolo superpuesto es un nivel de seguridad que agrega un protocolo al proceso de conexión de socket para realizar la autenticación y establecer un esquema de cifrado. Este protocolo de seguridad suele requerir los servicios de un protocolo de transporte subyacente y confiable, como TCP o SPX.

El término *Protocolo base* hace referencia a un protocolo, como TCP o SPX, que es totalmente capaz de realizar comunicaciones de datos con un punto de conexión remoto. Un *Protocolo por capas* es un protocolo que no puede ser independiente, mientras que una *cadena de protocolos* es uno o varios protocolos en capas agrupadosdos juntos y delimitados por un protocolo base.

Puede crear una cadena de protocolos si diseña los protocolos superpuestos para admitir Windows Sockets 2 SPI en los bordes superior e inferior. Una estructura especial de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) hace referencia a la cadena de protocolos en conjunto y describe el orden explícito en el que se unen los protocolos en capas. Esto se muestra en la ilustración siguiente. Dado que solo las aplicaciones pueden usar directamente los protocolos base y las cadenas de protocolo, son los únicos que se muestran cuando los protocolos instalados se enumeran con la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

![arquitectura de protocolo superpuesto](images/ovrvw2-3.png)

 

 
