---
description: En función de la taxonomía definida para los esquemas de multipunto o multidifusión independientes del protocolo Windows Sockets 2, ATM entra en la categoría de datos con raíz y planos de control con raíz.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Detalles de la función DE ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b089d02653ee996acc249f63144654c952ba724425fb208d9eb35cc9c2589e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051383"
---
# <a name="winsock-atm-function-details"></a>Detalles de la función DE ATM de Winsock

En función de la taxonomía definida para los esquemas de multipunto o multidifusión independientes del protocolo Windows Sockets 2, ATM entra en la categoría de datos con raíz y planos de control con raíz. (Consulte la especificación de api Windows Sockets 2, Apéndice D para obtener más información). Una aplicación que actúa como raíz crearía sockets raíz de c y los homólogos que se ejecutan en nodos \_ hoja utilizarían \_ sockets hoja de c. La aplicación raíz usará [**WSAJoinLeaf para**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) agregar nuevos nodos hoja. Las aplicaciones correspondientes en los nodos hoja habrán establecido sus sockets hoja c \_ en el modo de escucha. **WSAJoinLeaf** con un socket raíz de c especificado se asignará al mensaje SETUP de Q.2931 (para la primera hoja) o al mensaje ADD PARTY (para las hojas \_ posteriores).

> [!Note]  
> Los parámetros de QoS especificados en **WSAJoinLeaf** para las hojas posteriores deben omitirse según la especificación UNI del foro de ATM.

 

La combinación iniciada por hoja no forma parte del ATM UNI 3.1, pero se admite en LA UNI 4.0 de ATM. Por [**lo tanto, WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) con un socket hoja c especificado se puede asignar al \_ mensaje UNI 4.0 de ATM adecuado.

El parámetro AAL y la negociación B-LLI se admiten mediante la modificación de los IE correspondientes en el parámetro *lpSQOS* tras la invocación de la función de condición especificada en [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).

> [!Note]  
> Solo se pueden modificar determinados campos de esas dos E/S. Consulte el Apéndice C y el Apéndice F de la especificación DE LA UNI del foro de ATM para obtener más información.

 

 

 



