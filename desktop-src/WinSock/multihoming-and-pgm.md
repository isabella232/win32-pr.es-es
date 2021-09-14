---
description: Se debe prestar especial atención a los remitentes o receptores de PGM de varios dominios. En esta página se describen las consideraciones y se proporcionan directrices para los procedimientos recomendados de programación.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multi-host y PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172582"
---
# <a name="multihoming-and-pgm"></a>Multi-host y PGM

Se debe prestar especial atención a los remitentes o receptores de PGM de varios dominios. En esta página se describen las consideraciones y se proporcionan directrices para los procedimientos recomendados de programación.

## <a name="multihomed-pgm-sender"></a>Remitente de PGM de varios dominios

Cuando una aplicación no puede especificar una interfaz al llamar a la función [**connect,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) se usa la primera interfaz disponible. Si no hay ninguna interfaz disponible, se **produce un error en la** conexión.

Cuando una aplicación especifica una interfaz mediante la opción de socket [RM SET SEND \_ \_ \_ IF,](socket-options.md) se realiza implícitamente un intento de enlace [**a**](/windows/desktop/api/winsock/nf-winsock-bind) esa interfaz mediante TCP/IP y se produce un error si TCP/IP produce un error en la solicitud de enlace. Si la interfaz se establece mediante RM SET SEND IF varias veces, solo se puede aplicar correctamente el último \_ \_ conjunto de \_ interfaces.

Windows Sockets mantiene qué interfaz se establece y, si esa interfaz desaparece, la sesión se desconecta.

## <a name="multihomed-pgm-receiver"></a>Receptor DE PGM de varios entornos

Cuando una aplicación no puede especificar una interfaz al llamar a la función [**de**](/windows/desktop/api/Winsock2/nf-winsock2-listen) escucha, se usa la interfaz predeterminada. Si no hay ninguna interfaz disponible, se [**produce un error en**](/windows/desktop/api/winsock/nf-winsock-bind) el enlace.

Cuando una aplicación especifica una o varias interfaces en las que escuchar, mediante [RM \_ ADD RECEIVE \_ \_ IF](socket-options.md), Windows Sockets intenta enlazarse a la interfaz o interfaces solicitadas mediante TCP/IP. Cualquier error de TCP/IP hace que se produce un error en esta solicitud. A diferencia del caso del remitente de PGM, la adición de una interfaz de recepción varias veces hace que las escuchas se publiquen en todas las interfaces agregadas correctamente. Use la opción de socket RM \_ DEL RECEIVE IF para dejar de escuchar en una \_ \_ interfaz.

Windows Los sockets no mantienen el estado sobre varias interfaces de escucha especificadas y, en su lugar, se basa en TCP/IP para hacerlo. Sin embargo, una vez que una sesión está en curso, Windows Sockets realiza un seguimiento de la interfaz entrante para esa sesión y, si esa interfaz desaparece, Windows Sockets desconecta la sesión.

 

 



