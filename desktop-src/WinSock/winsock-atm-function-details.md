---
description: En función de la taxonomía definida para los esquemas multidifusión y multidifusión independientes del Protocolo de Windows Sockets 2, ATM entra en la categoría de los datos raíz y los planos de control raíz.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Detalles de la función ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155252"
---
# <a name="winsock-atm-function-details"></a>Detalles de la función ATM de Winsock

En función de la taxonomía definida para los esquemas multidifusión y multidifusión independientes del Protocolo de Windows Sockets 2, ATM entra en la categoría de los datos raíz y los planos de control raíz. (Consulte la especificación de la API de Windows Sockets 2, Apéndice D para obtener más información). Una aplicación que actúa como raíz crearía \_ Sockets raíz de c y los homólogos que se ejecutan en los nodos hoja usarían \_ sockets de hojas de c. La aplicación raíz usará [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregar nuevos nodos hoja. Las aplicaciones correspondientes en los nodos hoja habrán establecido sus \_ sockets de hoja c en el modo de escucha. **WSAJoinLeaf** con un \_ socket raíz de c especificado se asignará al mensaje de instalación Q. 2931 (para la primera hoja) o al mensaje de agregar entidad (para cualquier salida subsiguiente).

> [!Note]  
> Los parámetros de QoS especificados en **WSAJoinLeaf** para cualquier salida subsiguiente deben omitirse según la especificación UNI del Foro de ATM.

 

La combinación iniciada por hojas no forma parte del nodo ATM UNI 3,1, pero se admite en la plataforma ATM UNI 4,0. Por lo tanto, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) con un socket de hoja de c \_ especificado se puede asignar al mensaje unidireccional 4,0 de ATM adecuado.

El parámetro AAL y la negociación B-LLI se admiten a través de la modificación de la s correspondiente en el parámetro *lpSQOS* después de la invocación de la función de condición especificada en [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).

> [!Note]  
> Solo se pueden modificar ciertos campos de esas dos s. Consulte el Apéndice C y el Apéndice F del Foro de ATM para obtener más información.

 

 

 



