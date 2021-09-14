---
description: La interfaz de usuario (UI) de tarjeta inteligente es un único cuadro de diálogo común que permite al usuario especificar o buscar una tarjeta inteligente para abrir (es decir, conectarse a una aplicación y usarla en una aplicación).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Tarjeta inteligente Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071214"
---
# <a name="smart-card-user-interface"></a>Tarjeta inteligente Interfaz de usuario

La interfaz [*de*](../secgloss/u-gly.md) usuario (UI) [](../secgloss/s-gly.md) de tarjeta inteligente es un único cuadro de diálogo común que permite al usuario especificar o buscar una tarjeta inteligente para abrir (es decir, conectarse a una aplicación y usarla en una aplicación).

Las siguientes son dos maneras de usar el cuadro de diálogo común. Ambos asumen que se mostrará la interfaz de usuario del cuadro de diálogo. Para obtener más información, vea [**OPENCARDNAME.**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)

**Para seleccionar una tarjeta inteligente para abrir**

1.  Declare una variable de tipo **OPENCARDNAME.**
2.  Proporcione suficiente información en el cuadro de diálogo común para restringir la búsqueda de una tarjeta inteligente que la aplicación que realiza la llamada está buscando. Esto incluye especificar **lpstrGroupNames**, **lpstrCardNames** y **rgguidInterfaces.** Esto también incluye especificar un protocolo y un modo de recurso compartido preferidos que se usarán cuando el cuadro de diálogo común se conecte a la tarjeta mediante los miembros **dwShareMode** y **dwPreferredProtocols** de la estructura [**OPENCARDNAME.**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)
3.  Llame a [**la función GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) para mostrar el cuadro de diálogo común al usuario. Se mostrará una línea de información de ayuda sencilla y, si se encuentra una de las tarjetas que se solicitan, la tarjeta se resaltará en la pantalla. Para varias búsquedas de nombres de tarjeta, se resaltará el primer lector que contenga una de las tarjetas preferidas.
4.  A continuación, el usuario selecciona una tarjeta, hace clic **en Aceptar** y se conecta a la tarjeta inteligente.

**Para buscar una tarjeta específica**

1.  Declare una variable de tipo **OPENCARDNAME.**
2.  Proporcione suficiente información en el cuadro de diálogo común para restringir la búsqueda de una tarjeta inteligente que la aplicación que realiza la llamada está buscando. Esto incluye especificar **lpstrGroupNames**, **lpstrCardNames** y **rgguidInterfaces.**
3.  Cree las **Conectar** de devolución de llamada , **Check** y **Disconnect** y establezca los miembros de datos **lpfnConnect**, **lpfnCheck** y **lpfnDisconnect** correctamente.
    > [!Note]  
    > Las tres funciones y miembros deben estar disponibles cuando se usa el cuadro de diálogo común de esta manera.

     

4.  Llame a la función de cuadro de diálogo común [**GetOpenCardName.**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea)
5.  A continuación, el cuadro de diálogo común buscará las tarjetas solicitadas. Si se encuentra un nombre de tarjeta o una cadena [*ATR*](../secgloss/a-gly.md) correspondientes, las funciones de devolución de **llamada Conectar**, **Check** y **Disconnect** se llamarán en secuencia. Si una tarjeta pasa la **rutina Check** (es decir, la devolución de llamada **Check** devuelve **TRUE),** esta tarjeta se resalta en la pantalla al usuario.
    > [!Note]  
    > Si se dan varios nombres de tarjeta, el primer lector que contenga una de las tarjetas solicitadas y pase la **rutina Check** será la tarjeta seleccionada.

     

6.  Si no se encuentra ninguna coincidencia, aparecerá un cuadro de diálogo común.

 

 
