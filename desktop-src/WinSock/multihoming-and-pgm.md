---
description: Se debe tener especial en cuenta a los remitentes o receptores de PGM de varios destinos. En esta página se describen las consideraciones y se proporcionan directrices para los procedimientos recomendados de programación.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multi-host y PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e19ab149c8068c1a13f2c8089a567157618ef7287e8ef632145e5b934d626c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112089"
---
# <a name="multihoming-and-pgm"></a>Multi-host y PGM

Se debe tener especial en cuenta a los remitentes o receptores de PGM de varios destinos. En esta página se describen las consideraciones y se proporcionan directrices para los procedimientos recomendados de programación.

## <a name="multihomed-pgm-sender"></a>Remitente de PGM de varios destinos

Cuando una aplicación no puede especificar una interfaz al llamar a la función [**connect,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) se usa la primera interfaz disponible. Si no hay ninguna interfaz disponible, se **produce un error en la** conexión.

Cuando una aplicación especifica una interfaz mediante la opción de socket [RM SET SEND \_ \_ \_ IF,](socket-options.md) se realiza un intento de enlace implícitamente [**a**](/windows/desktop/api/winsock/nf-winsock-bind) esa interfaz mediante TCP/IP y se produce un error si TCP/IP produce un error en la solicitud de enlace. Si la interfaz se establece mediante RM SET SEND IF varias veces, solo se puede aplicar correctamente \_ el último conjunto de \_ \_ interfaces.

Windows Sockets mantiene qué interfaz se establece y, si esa interfaz desaparece, la sesión se desconecta.

## <a name="multihomed-pgm-receiver"></a>Receptor PGM de varios alojamientos

Cuando una aplicación no puede especificar una interfaz al llamar a la función [**de**](/windows/desktop/api/Winsock2/nf-winsock2-listen) escucha, se usa la interfaz predeterminada. Si no hay ninguna interfaz disponible, se [**produce un error en**](/windows/desktop/api/winsock/nf-winsock-bind) el enlace.

Cuando una aplicación especifica una o varias interfaces en las que se va a escuchar, mediante [RM \_ ADD RECEIVE \_ \_ IF](socket-options.md), Windows Sockets intenta enlazar a la interfaz o interfaces solicitadas mediante TCP/IP. Cualquier error de TCP/IP hace que se produce un error en esta solicitud. A diferencia del caso del remitente pgm, la adición de una interfaz de recepción varias veces hace que las escuchas se publiquen en todas las interfaces agregadas correctamente. Use la opción de socket RM \_ DEL RECEIVE IF para dejar de escuchar en una \_ \_ interfaz.

Windows Los sockets no mantienen el estado de varias interfaces de escucha especificadas y, en su lugar, se basa en TCP/IP para hacerlo. Sin embargo, una vez que una sesión está en curso, Windows Sockets realiza un seguimiento de la interfaz entrante de esa sesión y, si esa interfaz desaparece, Windows Sockets desconecta la sesión.

 

 



