---
description: 'Windows Sockets 2 incorpora el concepto de protocolo por capas: uno que implementa solo funciones de comunicaciones de nivel superior mientras se basa en una pila de transporte subyacente para el intercambio real de datos con un punto de conexión remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolos por capas y cadenas de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e60943bac5545fd7bb2bc87709d08c59d3addab205d14cab80687596721b973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858455"
---
# <a name="layered-protocols-and-protocol-chains"></a>Protocolos por capas y cadenas de protocolo

Windows Sockets 2 incorpora el concepto de protocolo por capas: uno que implementa solo funciones de comunicaciones de nivel superior mientras se basa en una pila de transporte subyacente para el intercambio real de datos con un punto de conexión remoto. Un ejemplo de este tipo de protocolo por capas es una capa de seguridad que agrega un protocolo al proceso de conexión de socket para realizar la autenticación y establecer un esquema de cifrado. Por lo general, este protocolo de seguridad requiere los servicios de un protocolo de transporte subyacente y confiable, como TCP o SPX.

El término *protocolo base* hace referencia a un protocolo, como TCP o SPX, que es totalmente capaz de realizar comunicaciones de datos con un punto de conexión remoto. Un *protocolo por* capas es un protocolo  que no puede estar solo, mientras que una cadena de protocolos es uno o varios protocolos en capas unidos y delimitados por un protocolo base.

Puede crear una cadena de protocolos si diseña los protocolos en capas para admitir el SPI Windows Sockets 2 en sus bordes superior e inferior. Una estructura [**info de \_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial hace referencia a la cadena de protocolos en su conjunto y describe el orden explícito en el que se unen los protocolos por capas. Esto se muestra en la ilustración siguiente. Dado que solo las aplicaciones pueden usar directamente los protocolos base y las cadenas de protocolos, son los únicos que se enumeran cuando los protocolos instalados se enumeran con la función [**WSAEnumProtocols.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)

![Arquitectura de protocolos por capas](images/ovrvw2-3.png)

 

 
